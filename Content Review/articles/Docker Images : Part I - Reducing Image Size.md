Notes for Docker Images - Part I - Reducing Image Size

## Source:
Author: ardanlabs.com
Category: articles
Updated: 12/26/2021 10:10 AM
Highlights URL: https://readwise.io/bookreview/1548110
SourceUrl: https://www.ardanlabs.com/blog/2020/02/docker-images-part1-reducing-image-size.html

%%1548110topstart%%
#### Extras:
[[Docker]][[multi-stage builds]]
%%1548110topend%%
 
-----
 ## Highlights:

### multi-stage builds, because that’s where anyone should start...
>multi-stage builds, because that’s where anyone should start if they want to reduce the size of their images ^rw43203497hl


Highlighted: 03/12/2020 11:06 AM
Updated: 12/26/2021 10:10 AM

%%43203497start%%
#### Extras:

%%43203497end%%

------

### We obtain a multi-stage build by adding another FROM line in...
>We obtain a multi-stage build by adding another FROM line in our Dockerfile. Look at the example below
&gt;FROM gcc AS mybuildstage
COPY hello.c .
RUN gcc -o hello hello.c
FROM ubuntu
COPY --from=mybuildstage hello .
CMD [&quot;.&#x2F;hello&quot;] ^rw262419430hl


Highlighted: 12/26/2021 09:24 AM
Updated: 12/26/2021 10:10 AM
https://instapaper.com/read/1283413103/18338357

%%262419430start%%
#### Extras:

%%262419430end%%



------

### You don’t have to use the AS keyword when declaring your bui...
>You don’t have to use the AS keyword when declaring your build stage. When copying files from a previous stage, you can simply indicate the number of that build stage (starting at zero
&gt;In other words, the two lines below are identical
&gt;COPY --from=mybuildstage hello .
COPY --from=0 hello . ^rw262419431hl


Highlighted: 12/26/2021 09:25 AM
Updated: 12/26/2021 10:10 AM
https://instapaper.com/read/1283413103/18338364

%%262419431start%%
#### Extras:

%%262419431end%%



------

### strongly recommend that you stick to classic images for your...
>strongly recommend that you stick to classic images for your “run” stage. By “classic”, I mean something like CentOS, Debian, Fedora, Ubuntu; something familiar. You might have heard about Alpine and be tempted to use it. Do not! At least, not yet. We will talk about Alpine later, and we will explain why we need to be careful with it. ^rw262419432hl


Highlighted: 12/26/2021 09:26 AM
Updated: 12/26/2021 10:10 AM
https://instapaper.com/read/1283413103/18338366

%%262419432start%%
#### Extras:

%%262419432end%%



------

### Personally, I wouldn’t go with the scratch images (because t...
>Personally, I wouldn’t go with the scratch images (because troubleshooting them might be, well, trouble) but if that’s what you’re after, they’re here for you! ^rw262419433hl


Highlighted: 12/26/2021 09:32 AM
Updated: 12/26/2021 10:10 AM
https://instapaper.com/read/1283413103/18338380

%%262419433start%%
#### Extras:

%%262419433end%%



------

