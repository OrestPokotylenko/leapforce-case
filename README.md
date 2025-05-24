## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### HubSpot CMS Custom Fields Proposal

Below is a proposal for the custom fields required to make the “CTA Section - Two Blocks” fully editable by a marketeer or project manager in HubSpot CMS.

| Field Label                | Required/Optional | Default Value                                      | Tooltip / Help Text                                               | Constraints                                  |
|----------------------------|-------------------|----------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------|
| Label                      | Optional          | Why choose us?                                     | Short label above the main heading                                | Max 50 characters                            |
| Title Before Highlight     | Required          | Get the help you need from                         | Text before the highlighted call-to-action in the main heading    | Max 100 characters                           |
| Call-to-Action             | Required          | certified local professionals                      | Highlighted text in the main heading                              | Max 60 characters                            |
| Title After Highlight      | Required          | you can trust                                      | Text after the highlighted call-to-action in the main heading     | Max 100 characters                           |
| Body Text                  | Optional          | We design and develop websites that not only look beautiful but drive real results. Let’s take your digital presence to the next level. | Main descriptive text below the heading                           | Max 300 characters, multiline allowed        |
| Optional Button            | Optional          | Let's talk                                         | Text for the optional call-to-action button                       | Max 30 characters                            |
| Section 1 Title            | Required          | Website Development                                | Title for the first content block                                 | Max 60 characters                            |
| Section 1 Text             | Required          | Custom-built websites tailored to your business needs with a focus on speed, SEO, and conversion. | Description for the first content block                           | Max 200 characters, multiline allowed        |
| Section 2 Title            | Required          | Digital Strategy                                   | Title for the second content block                                | Max 60 characters                            |
| Section 2 Text             | Required          | We help you define a digital roadmap to achieve your goals — from marketing automation to content strategy. | Description for the second content block                          | Max 200 characters, multiline allowed        |


### ArrowButton en ArrowButtonSection

Het Figma-document bevatte geen ontwerp voor een witgekleurde ArrowButton. Daarom heb ik zelf twee verschillende versies uitgewerkt.