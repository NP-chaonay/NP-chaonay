// THIS IS NOT CODE, BUT THE DRAFT OF "NP-chaonay" STANDARD ON STUFF SUCH AS CODING, SOURCE-CODE-COLLABORATION; BUT NOT LIMITED TO.

# Coding
## Documenting/Commenting
- Accoding to the standard, the operation is to do either/both documenting and/or commmenting on each parts of code, and must follow to the given standard's guideline. The containing place for documenting/commmenting is not stricted, you can place it on most-top/most-bottom/separated-file/etc. .
- Beware that not only: complex, generally-not-understand;-- thing that needs it; the easy/code code also need this procedure too. But if we do this on all easy/simple code, it would be very necessary and may be weird. This guideline tells what should you explains. Specially on easy/simple code, misssing this procedure would cause further problem on further debugging or interpreting.
	- So just think that this procedure helps you to visualize the outline and brief program's operation; in case of complex code/thing comes to the mind/coders, this also helps to understand too.
- For commenting
	- The code comments must follow the template (if the kind of code is in defined list of categories) (not stricted on formatting but what the comment contains and some syntax); if not availiable, then pass this.
		- If the part of code is not belong to categories for commenting, you can comment it in general way that follows the standard.
		- You may blank the field, but this is very unrecommended (so it is not forbidded) according to the standard. Try to comment something even simple in 1 sentence, this is also acceptable and considered as good comment rather than blank it at all.
	- try to explain brief information in first short passage or in first a few sentences; also it is better practice to put the remained long passage of explaination into separate documentation. However it is not forbidded to put long passage into commenting (such as standalone code), however you should make it easy to read. (for example limit line width of passage)
	- It is not stricted to comment only on top or bottom of the code line, the standard only enforce to explain the code in some place, either/both commenting or documentating.
### What should I explains
- New variable declaration, tell what it is contains (not only for first-time containing but further), the objective, and how to using it
= New function defination, tell what function does (including what it does return), how to use (such as acccept-argument-type and guideline on argument value)
	- For code inside the function defination, uses the suitable guideline.
	- This also appiled on methods or function of class.
	- The function parameters are also appiled by "New variable declaration" guideline, but with information of "Acceptable-Value", see the template section below for the more information.
- New class defination, tell the objective, how to using it, what it can do.
	- Beware that methods or function of class also appiled by guideline on "New function defination"
	- For code inside the class defination, uses the suitable guideline.
- For other class-like defination, uses guideline on "New class defination"
- For other function-like defination, uses guideline on "New function defination"
- Tell its objective and what it does; for:
	- for/while/etc. loop
	- conditional block
- For keywords/operations that should be explain, tell its objective, what it does.
	- For example: Kind of most arithmetic operation can be able to not be explained, for example the code "1%1", the code is already easily to be read by people.
- For Exception-catching block, tell its objective (also to tell why you need to catch the exception), catch what kind of error/exception, what the normal code do and what exception handling code do
- New object creation that created from class's object initialization, and the final object is not function/function-alike/class/class-alike: tell the objective, how to use (optional)
### Template
> "ReferTo" Field can be ignore, this field is for tell what reference/identifier [key]word we mention to. You can reference to multiple reference/identifier for shorter commenting.

> "AdditionalInfo" Field can be ignore, this field is for additional information.
#### New Variable Declaration
```python
## [Variable-Docs] (ReferTo: -)
# Objective:
# For-Contains:
# How-To-Use:
# AdditionalInfo: -
```
#### New Function/Function-alike Defination
```python
## [Function-Docs] (ReferTo: -)
# Do-What:
# How-To-Use:
# Parameters:
# - var_name (var_type)
#     Objective:
#     For-Contains:
#     Acceptable-Value:
#     How-To-Use:
# Return-What:
# AdditionalInfo: -
```
#### New Class/Class-alike Defination
```python
## [Class-Docs] (ReferTo: -)
# Objective:
# What-Can-Do:
# How-To-Use:
# AdditionalInfo: -
```
#### for/while/etc. Loop
```python
## [Loop-Docs] (ReferTo: -)
# Objective:
# AdditionalInfo: -
```
#### Conditional Block
```python
## [ConditionalBlock-Docs] (ReferTo: -)
# Objective:
# AdditionalInfo: -
```
#### Keywords/Operations that should be explain
```python
## [KeywordAndOp-Docs] (ReferTo: -)
# Objective:
# AdditionalInfo: -
```
#### Exception Catching Block
```python
## [ExceptionCatching-Docs] (ReferTo: -)
# Objective:
# Catch-What:
# What-Normal-Code-Do:
# What-ExceptionHandling-Code-Do:
# AdditionalInfo: -
```
#### Object Creation that created from class's object initialization
```python
## [ObjectFromClassInit-Docs] (ReferTo: -)
# Objective:
# How-To-Use:
# AdditionalInfo: -
```
> How-To-Use can be blank (recommended than remove it) because it is optional.
### Example
```python
def index_to_no(i): return i+1
```
> In above code, according to the standard, we have to comment/document these thing
>	- what function do: Receive indexing number and convert to ordering number in counting-manner (1st using 1 for the ordering instead of 0 which is in indexing-manner)
>	- how to use 1st parameter (this question also answers how to use the function): receiving integer of indexing-manner number
>	- what does the function return (this question also answers how to use the function): converted value in int

> however "return i+1" doesn't require the commenting, because there is answer on questions on function, questions already tell how and why that code do the thing. You just comment on the function code that it is necessary to do.
```python
# This demostrating code has syntax based on Python, but not exactly same as Python code. This code's objective is to show how to apply the mentioned commenting standard on the simple code of program.

## [Variable-Docs] (ReferTo: all variables that allocated for imported headers)
# Objective: -
# For-Contains: -
# How-To-Use: -
# AdditionalInfo: -
# Import necessary headers
import stdlib,linuxsys.{.,io,stdio}

## [Variable-Docs] (ReferTo: -)
# Objective: accessing stdout through fd number
# For-Contains: fd of stdout
# How-To-Use: use as fd number
# AdditionalInfo:
# 	- readonly because 1x defining
# 	- linuxsys.stdio.stdout.fd gives uint8, so using uint8
# 	- no init value for fast declaration
var readonly stdlib.uint8 stdout_fd

## [Variable-Docs] (ReferTo: -)
# Objective: string for printing to stdout
# For-Contains: message for printing
# How-To-Use: -
# AdditionalInfo:
# 	- readonly because 1x defining
var readonly stdlib.chararray stdout_msg "Hello, World!\n"

## [Variable-Docs] (ReferTo: -)
# Objective: acts as literal of 0
# For-Contains: uint8, zero value
# How-To-Use: -
# AdditionalInfo:
# 	- readonly because it is literal
# 	= using literal for good practice
var readonly stdlib.uint8 uint8_0 0

setvar stdout_fd linuxsys.stdio.stdout.fd
linuxsys.io.writestream(stdout_fd,stdout_msg)
linuxsys.exit(uint8_0)
```
> in above code, some comments using unrecomended way to comment, this can be used however you have to ensure that the blanked comment is not make thing worse.

> we don't have to explain "linuxsys.stdio.stdout.fd" and so on, because the all argument have been explained, and the itself defination's explaination can be see on the respounding header, so no need to re-explain.

> See that, the explaination related to language implementation or imported object is reduced due to above reason (for imported object) and langauge implementation is thing that coder should know before works on it.