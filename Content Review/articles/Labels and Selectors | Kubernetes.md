Notes for Labels and Selectors | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/03/2021 03:39 PM
Highlights URL: https://readwise.io/bookreview/8080591
SourceUrl: https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/

%%8080591topstart%%
#### Extras:
**kubernetes**
%%8080591topend%%
 
-----
 ## Highlights:

### Unlike names and UIDs, labels do not provide uniqueness. In ...
>Unlike names and UIDs, labels do not provide uniqueness. In general, we expect many objects to carry the same label(s). ^rw153046149hl


Highlighted: 03/03/2021 03:37 PM
Updated: 03/03/2021 03:37 PM

%%153046149start%%
#### Extras:

%%153046149end%%

------

### Via a label selector, the client/user can identify a set of ...
>Via a label selector, the client&#x2F;user can identify a set of objects. The label selector is the core grouping primitive in Kubernetes ^rw153046161hl


Highlighted: 03/03/2021 03:38 PM
Updated: 03/03/2021 03:38 PM

%%153046161start%%
#### Extras:

%%153046161end%%

------

### The API currently supports two types of selectors: equality-...
>The API currently supports two types of selectors: equality-based and set-based ^rw153046172hl


Highlighted: 03/03/2021 03:38 PM
Updated: 03/03/2021 03:38 PM

%%153046172start%%
#### Extras:

%%153046172end%%

------

### Equality- or inequality-based requirements allow filtering b...
>Equality- or inequality-based requirements allow filtering by label keys and values. Matching objects must satisfy all of the specified label constraints, though they may have additional labels as well. Three kinds of operators are admitted =,==,!=. The first two represent equality (and are synonyms), while the latter represents inequality. ^rw153046219hl


Highlighted: 03/03/2021 03:39 PM
Updated: 03/03/2021 03:39 PM

%%153046219start%%
#### Extras:

%%153046219end%%

------

### Set-based label requirements allow filtering keys according ...
>Set-based label requirements allow filtering keys according to a set of values. Three kinds of operators are supported: in,notin and exists (only the key identifier). ^rw153046351hl


Highlighted: 03/03/2021 03:39 PM
Updated: 03/03/2021 03:39 PM

%%153046351start%%
#### Extras:

%%153046351end%%

------

