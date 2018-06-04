- Start Date: 2018-05-29
- RFC PR: https://github.com/biotope/rfcs/pull/2
- Project:

# Summary

We should add a biotope CLI to be able to run ```biotope generate``` to generate a component or ```biotope report``` to report a bug.

# Motivation

A nice abstraction layer. One can choose to use biotope-cli for more features, which will not come with the default biotope package.
Biotope itself gets more slim!


# Detailed design

The current idea for features only available through the CLI would be:

- ```biotope report```: Will log all the information needed for a bug report (node version, yarn version, biotope version, ...)
- ```biotope generate```: Will use the biotope generator to generate biotope components.


# Drawbacks



# Alternatives



# Unresolved questions
- Optional features: ```biotope start```, ```biotope build```
