# Chain Reaction Pattern

A reaction of a rule can trigger a new event that invokes subsequent rules. In turn, these subsequent rules may have reactions that again invoke rules, leading to a chain of reactions. The Chain Reaction pattern consists of consecutive loaded rules and of indirect reactions which lead to a cascade of triggered rules with their corresponding reactions.

Active rules are processed asynchronously to avoid coordination and waiting. Coupling of data and visuals or audio can be achieved by observing state changes.

| on:command	| →	| do:assign |
|---|---|---|
> data.flag = 1

| as:stated	| if:data.flag == 1	| do:say | 
|---|---|---|
> "Indirect Reaction Pattern" 🗣

## Examples

| ARchi VR |
|:---:|
| [Button places Box](../examples/ARchiVR/button-places-box/description.md) |
| <img align="right" src="../examples/ARchiVR/button-places-box/preview.gif" width="150px" /> |