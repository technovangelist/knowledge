great cross-shell prompt
Source: https://starship.rs/

**shell prompt**
I have all my dev projects in a projects directory. Under that there is a datadog (my employer) directory and a technovangelist directory. I have it call out what dir I am under.


My config:
~/.config/starship.toml
```toml
[aws]
disabled=true

[custom.datadogprojects]
command = "echo DD Projects"  # shows output of command
when = """ string match '*projects/datadog*' $PWD """
prefix = " in "

[custom.technovangelistprojects]
command = "echo tvlst Projects"  # shows output of command
when = """ string match '*projects/technovangelist*' $PWD """
prefix = " in "
[directory]
fish_style_pwd_dir_length=1
truncation_length = 2
[time]
disabled=false
time_format = "🕙[ %T ]"
```
