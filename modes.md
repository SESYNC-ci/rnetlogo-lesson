---
---

Run RNetLogo using `NLStart()`. Use the `gui =` argument to control which mode to operate in. 


| Mode | Control in R | Control in NetLogo | Multiple NetLogo sessions |
|------|-------------------------|---------------------------|
| GUI  | yes | yes | no |
| Headless | yes | no | yes |



~~~r
NLStart(nl.path, gui = FALSE)
~~~
{:.input}
