Notes for 10 Bad TypeScript Habits to Break This Year

## Source:
Author: startup-cto.net
Category: articles
Updated: 02/02/2021 11:35 AM
Highlights URL: https://readwise.io/bookreview/7503500
SourceUrl: https://startup-cto.net/10-bad-typescript-habits-to-break-this-year/

%%7503500topstart%%
#### Extras:
**typescript** 
%%7503500topend%%


 
-----
 ## Highlights:

### Optional properties
>Optional properties ^rw140413612hl

Comment: In the list of habits to stop. I have plenty of this.
Suggests that 

```
interface Product {
  id: string
  type: 'digital' | 'physical'
  weightInKg?: number
  sizeInMb?: number
}
```

 is bad and this is much better: 

```
interface Product {
  id: string
  type: 'digital' | 'physical'
}

interface DigitalProduct extends Product {
  type: 'digital'
  sizeInMb: number
}

interface PhysicalProduct extends Product {
  type: 'physical'
  weightInKg: number
}
```
need to play with it ^rw140413612comment

Highlighted: 02/02/2021 11:31 AM
Updated: 02/02/2021 11:35 AM

%%140413612start%%
#### Extras:
#OptionalProperties
%%140413612end%%



------

### return products as Product[]
>return products as Product[] ^rw140412770hl

Comment: I have certainly done this. I have plenty of myvar as unknown as string ^rw140412770comment

Highlighted: 02/02/2021 11:29 AM
Updated: 02/02/2021 11:29 AM

%%140412770start%%
#### Extras:

%%140412770end%%



------

### ??, unlike ||, falls back only for null or undefined, not fo...
>??, unlike ||, falls back only for null or undefined, not for all falsy values. Also, if your functions are so long that you cannot define defaults at the beginning, then splitting them might be a good idea ^rw140412667hl

Comment: Hmm, need to experiment with ?? vs || ^rw140412667comment

Highlighted: 02/02/2021 11:27 AM
Updated: 02/02/2021 11:27 AM

%%140412667start%%
#### Extras:

%%140412667end%%



------

### {
  "compilerOptions target": "ES2015 module...
>{
  "compilerOptions
>target": "ES2015
>module": "commonjs
>strict": true
  }
} ^rw140412432hl

Comment: always use strict mode in ts ^rw140412432comment

Highlighted: 02/02/2021 11:24 AM
Updated: 02/02/2021 11:25 AM

%%140412432start%%
#### Extras:

%%140412432end%%



------

