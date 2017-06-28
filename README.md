# proofmacros
Latex macros for logical proofs of programs

## Usage
In order to use the proofmacro's you will have to copy the `proofmacros.sty` file from [the repo](https://github.com/tosti007/proofmacros) into the same directory as your main latex file. Then you will have to include the package into your latex file like so: `\usepackage{proofmacros}`. This should be all the setup that you need.

The commands and enviroments that this package provides are listed below.

## Environments:
| Type     | Syntax
| -------- | ------
| proof    | `\begin{proof}[optional prefix]{name}`
| subproof | `\begin{subproof}[optional name]`
| eqproof  | `\begin{eqproof}[optional name]{starting value}`


## Commands:
| Command | Description | Syntax | Additional Info
| ------- | ----------- | ------ | ---------------
| some    | Print a some declaration on the screen | `\some{variable name}` | To be used inside steps/assumptions or goals, example result: [some i]
| assume  | Declare an assumption for your proof | `\assume{assumption value}` | Not to be used inside an Equational Proof
| goal    | Declare an goal | `\goal{goal value}` | Simmilair to assume, also not to be used inside an Equational Proof
| step    | Make an proof step | `\step{hint}{value}` | To be used for both normal Proofs and Equational Proofs
| done    | Conclude the proof to be done | `\done[optional different goal index]{hint}` | This is optional, you might as well use the step command for this

# Note:
* The delimiter between the hint and expression is defined in the `proofdelimiter`, you won't need to use this manually. However if you want to change it you can by using `\renewcommand{\proofdelimiter}{your delimiter}`
* If there is anything wrong or you feel like there should be an improvement don't hesitate to make an issue or send me a pull request on [github](https://github.com/tosti007/proofmacros/)!

---

Derived from http://www.cs.uu.nl/docs/vakken/pc/1617/supplements/pncproofmacros.sty by dr. S.W.B. Prasetya

By Brian Janssen, https://github.com/tosti007/proofmacros/
