# Hreflang

## Configuration

Stores > Configuration > ECWHIM SEO > General > Hreflang

![Configuring the Hreflang Extension](../images/extension/hreflang/configuration.png){ loading=lazy }

Set **Enable** to `Yes` to see more settings.

![Full Configuring the Hreflang Extension](../images/extension/hreflang/full-configuration.png){ loading=lazy }

| FIELD                                       | DESCRIPTION |
| ------------------------------------------- | ----------- |
| Enable              | Determines if the hreflang functionality is enabled. Options: Yes / No |
| Enable on           | Determines the types of pages for which the hreflang functionality is enabled. Options: Product Page / Category Page / CMS Page / Home Page |
| Scope               | Determines the scope within which the localized versions of the page should be linked. Options: <br> **Website** - Links localized versions of a page within each individual website. <br> **Global** - Links localized versions of a page across all websites. |
| Language Code       | Determines the supported language code that the version of the page is targeting. If set to `Use from Store Locale`, the language code is used from the **Locale** setting (Stores > Configuration > GENERAL > General > Locale Options). |
| Country Code        | Determines the supported region code that the version of the page is targeting. If set to `Use Default Country Code`, the region code is used from the **Default Country** setting (Stores > Configuration > GENERAL > General > Country Options). If set to `Do not add`, the region code will not be added to the value of the hreflang attribute. |
| x-default           | In the group of localized versions of the page, determines the store view whose page will have the value of the hreflang attribute `x-default`. |
| Relate CMS Pages by | Determines the CMS page attribute by which to link localized versions of the page. Options: ID / URL Key / Hreflang Identifier |

## Individual settings for entities

### CMS Page

Open the CMS page in edit mode and expand the _Search Engine Optimization_ section.

![CMS Page settings added by the Hreflang Extension](../images/extension/hreflang/cms-pages.png){ loading=lazy }

| FIELD               | DESCRIPTION |
| ------------------- | ----------- |
| Hreflang Identifier | An identifier that is used to link localized versions of the page. |
