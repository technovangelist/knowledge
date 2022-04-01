Notes for Secure Publication of Datadog Agent Integrations With TUF and In-Toto | Datadog

## Source:
Author: Trishank Karthik Kuppusamy
Category: articles
Updated: 02/03/2021 10:14 AM
Highlights URL: https://readwise.io/bookreview/7522893
SourceUrl: https://www.datadoghq.com/blog/engineering/secure-publication-of-datadog-agent-integrations-with-tuf-and-in-toto/

%%7522893topstart%%
#### Extras:

%%7522893topend%%


 
-----
 ## Highlights:

### Interested readers may also wish to consult our KubeCon 2018...
>Interested readers may also wish to consult our KubeCon 2018 talk and 28th USENIX Security Symposium technical paper for more details ^rw140913207hl

Comment: [](https://www.youtube.com/watch?v=XAlvd4QXngs&feature=emb_imp_woyt) ^rw140913207comment

Highlighted: 02/03/2021 10:13 AM
Updated: 02/03/2021 10:14 AM

%%140913207start%%
#### Extras:

%%140913207end%%



------

### To do so, we use two key pieces of technology: The Update Fr...
>To do so, we use two key pieces of technology: The Update Framework (TUF) and in-toto. The CI/CD system uses TUF to sign new integrations, and in-toto guarantees that the CI/CD system packaged exactly the source code that one of our developers signed. It is important to note that neither technology on its own is sufficient to deliver the desired security guarantees. But by tightly integrating both, we are contributing to our industry’s efforts to make the secure publication of software a standard as opposed to a nice-to-have ^rw140912712hl

Comment: how to protect the integrity of the build of the datadog agent ^rw140912712comment

Highlighted: 02/03/2021 10:11 AM
Updated: 02/03/2021 10:11 AM

%%140912712start%%
#### Extras:

%%140912712end%%



------

