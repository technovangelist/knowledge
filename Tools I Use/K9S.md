Super cool CLI tool for managing **kubernetes**

![screen_po.png](https://github.com/derailed/k9s/blob/master/assets/screen_po.png?raw=true)

| Action                                                         | Command                       | Comment                                                                |
|----------------------------------------------------------------|-------------------------------|------------------------------------------------------------------------|
| Show active keyboard mnemonics and help                        | \`?\`                           |                                                                        |
| Show all available resource alias                              | \`ctrl-a\`                      |                                                                        |
| To bail out of K9s                                             | \`:q\`, \`ctrl-c\`                |                                                                        |
| View a Kubernetes resource using singular/plural or short-name | \`:\`po⏎                        | accepts singular, plural, short-name or alias ie pod or pods           |
| View a Kubernetes resource in a given namespace                | \`:\`alias namespace⏎           |                                                                        |
| Filter out a resource view given a filter                      | \`/\`filter⏎                    | Regex2 supported ie \`fred|blee\` to filter resources named fred or blee |
| Inverse regex filer                                            | \`/\`! filter⏎                  | Keep everything that \*doesn't\* match.                                  |
| Filter resource view by labels                                 | \`/\`-l label-selector⏎         |                                                                        |
| Fuzzy find a resource given a filter                           | \`/\`-f filter⏎                 |                                                                        |
| Bails out of view/command/filter mode                          | \`<esc>\`                       |                                                                        |
| Key mapping to describe, view, edit, view logs,...             | \`d\`,\`v\`, \`e\`, \`l\`,...         |                                                                        |
| To view and switch to another Kubernetes context               | \`:\`ctx⏎                       |                                                                        |
| To view and switch to another Kubernetes context               | \`:\`ctx context-name⏎          |                                                                        |
| To view and switch to another Kubernetes namespace             | \`:\`ns⏎                        |                                                                        |
| To view all saved resources                                    | \`:\`screendump or sd⏎          |                                                                        |
| To delete a resource (TAB and ENTER to confirm)                | \`ctrl-d\`                      |                                                                        |
| To kill a resource (no confirmation dialog!)                   | \`ctrl-k\`                      |                                                                        |
| Launch pulses view                                             | \`:\`pulses or pu⏎              |                                                                        |
| Launch XRay view                                               | \`:\`xray RESOURCE \[NAMESPACE\]⏎ | RESOURCE can be one of po, svc, dp, rs, sts, ds, NAMESPACE is optional |
| Launch Popeye view                                             | \`:\`popeye or pop⏎             | See https://popeyecli.io                                               |