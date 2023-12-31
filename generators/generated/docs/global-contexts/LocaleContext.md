# LocaleContext

A [GlobalContext](/taxonomy/reference/global-contexts/overview.md) describing the users' language ([ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)) and country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements)).

import Mermaid from '@theme/Mermaid'

<Mermaid chart={`
    graph LR
      AbstractContext["AbstractContext<span class='properties'>id: string<br /></span>"] --> AbstractGlobalContext;
      AbstractGlobalContext -->       LocaleContext["LocaleContext<span class='properties'>language_code?: string<br />country_code?: string<br /></span>"];
    class LocaleContext diagramActive
  `}
  caption="Diagram: LocaleContext inheritance"
  baseColor="blue"
  links={[
{ name: 'AbstractGlobalContext', to: '/taxonomy/global-contexts' },   ]}
/>

### Properties

|                                 | type   | description                                                                   |
|:--------------------------------|:-------|:------------------------------------------------------------------------------|
| **language\_code _[optional]_** | string | Case sensitive ISO 639-1 language code. E.g. en, nl, fr, de, it, etc.         |
| **country\_code _[optional]_**  | string | Case sensitive ISO 3166-1 alpha-2 country code. E.g. US, NL, FR, DE, IT, etc. |
### Inherited Properties

|        | type   | description                                                                                                |
|:-------|:-------|:-----------------------------------------------------------------------------------------------------------|
| **id** | string | A unique string identifier to be combined with the Context Type (`_type`) for Context instance uniqueness. |

:::info setting of properties
The tracker can automatically set the `id` when using the official Plugin. On manual creation, `id` must be provided. 
:::
