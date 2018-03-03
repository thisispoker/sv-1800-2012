# SystemVerilog-1800-2012 README

This extension incorporates syntax highlighting and snippet support for `IEEE Std 1800-2012 - SystemVerilog` hardware description language and `Universal Verification Methodology` (UVM) in [Visual Studio Code](https://code.visualstudio.com/).

# Features
* Syntax highlighting and basic syntax checking capabilites for SystemVerilog.
* Scope start end checking for *module-endmodule*, *fork-join*, *begin-end*, etc.
* UVM class and type integration ()
* Snippet support for the verification side of SV and UVM

![Screenshot](https://github.com/gvekony/sv-1800-2012/raw/master/images/sv_screenshot_vs_code_dark.png)

## Fully or partially supported SystemVerilog-2012-1800 features
* checkers
* classes
* comments, attributes, various conventional highlights (accessors, numbers, etc.)
* constraint blocks
* coverage, covergroups
* interfaces, modports, clocking blocks
* modules
* packages
* programs
* tasks and functions
* user-defined primitives

### SV Snippets
SystemVerilog snippets are available with a `sv_` prefix.

* Containers: sv_module, sv_interface, sv_class
* Language constructs: sv_block_parallel, sv_block_sequential, sv_if, sv_if_blocks, sv_if_blocks_labels

As VS Code uses clever search in words and snippets pressing `sq` will most likely result in `sv_block_sequential` so you don't need to type the whole snippet expression. :)

## UVM
UVM classes, macros and functions are partially supported, implementation is work in progress.

### UVM Snippets
The most common UVM boilerplates are available with an `uvm_` prefix.

* UVM containers: uvm_class_object, uvm_class_object_params, uvm_class_component, uvm_class_component_params
* Macros (field macros are purposely omitted): uvm_macro_info, uvm_macro_warning, uvm_macro_error, uvm_macro_object_utils, etc.
* Phases: uvm_phase_build, uvm_phase_connect, etc.

![Snippets](https://github.com/gvekony/sv-1800-2012/raw/master/images/vs_code_snippets.gif)

## Indentation rules
* Indentation rules are added for the common constructs of SystemVerilog (eg.: module-endmodule, begin-end, etc.) for VS Code's `reindent` function
* As VS Code uses tmLanguage (TextMate) styled rules for this, there is no multiline support, eg. block comments can break your indentation if a line starts with begin for example.

## Extra folding rules
* Extra folding (but not indentation) rules are set for SystemVerilog compiler directives (eg.: ifndef-endif, pragma protect begin-end, etc.)
* Similarly to indentation rules, line breaked `` `pragma protect begin`` break this feature.

# Release Notes

## 1.0.4
Fixed scoping on extern defined construct, to have the correct scopes defined for their namespaces and names.

# Known bugs
* AND property/sequence operator and AND gate level primitive is not yet distinguished.


# License information

[MIT](https://github.com/gvekony/sv-1800-2012/blob/master/LICENSE.md) &copy; **Gergo Vekony**
