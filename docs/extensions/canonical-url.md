# Canonical URL

## Configuration

Stores > Configuration > ECWHIM SEO > General > Canonical URL

![Configuring the Canonical URL Extension](../images/extension/canonical-url/configuration.png){ loading=lazy }

Set **Enable** to `Yes` to see more settings.

![Full Configuring the Canonical URL Extension](../images/extension/canonical-url/full-configuration.png){ loading=lazy }

| FIELD                                       | DESCRIPTION |
| ------------------------------------------- | ----------- |
| Enable                                      | Determines if the canonical URL functionality is enabled. Options: Yes / No |
| Product Canonical URL Type                  | Determines which product URL will be used as the canonical URL. If your catalog is configured to include the category path in product URLs, your store will generate multiple URLs that point to the same product page: <br> 1. https://example.com/product.html <br> 2. https://example.com/category/product.html <br> 3. https://example.com/category/subcategory/product.html <br> Options: <br> **Without Categories Path** - Uses the product URL without the category path. (1) <br> **Min nesting of Categories** - Uses the product URL with minimal category nesting. (2) <br> **Max nesting of Categories** - Uses the product URL with maximum category nesting. (3) |
| Use parent Canonical URL for child products | Determines the product types whose child products will have the same canonical URL as the canonical URL of the parent product. Options: Configurable / Grouped / Bundle |
| Home Page Canonical URL Type                | Determines whether the home page canonical URL should contain a trailing slash. Options: Without a Trailing Slash / With a Trailing Slash |
| Canonical URL for Paginated Pages           | Determines whether the canonical URL of paginated pages should contain a pagination parameter (`?p=n`). Options: Without Page Parameter / With Page Parameter |
| Add rel="prev/next" link to Paginated Pages | Determines whether to include a rel="prev/next" link in the `<head>` section of paginated pages. Options: Yes / No |
| Canonical URL for Filtered Pages            | Determines whether the canonical URL of filtered pages should contain a filter parameters or it should not be used at all on this type of page. Options: Without Filter Parameters / With Filter Parameters / Do not add |
| Cross-domain                                | If there are multiple stores with the same or very similar content, this option helps set up a cross-domain canonical URL to avoid duplicate content. |
| Cross-domain URL	                          | The base URL of the store that is outside of the current Magento 2 installation. |

## Individual settings for entities

### Product

Open the product in edit mode and expand the _Search Engine Optimization_ section.

![Product settings added by the Canonical URL Extension](../images/extension/canonical-url/products.png){ loading=lazy }

| FIELD         | DESCRIPTION |
| ------------- | ----------- |
| Canonical URL | The URL that is used as the canonical URL for this product. For example: <br> _https://cross-domain.com/product.html_ <br> Set a relative URL to use the URL of another product or entity within the current store view. For example: <br> _other-product.html_ |

### Category

Open the category in edit mode and expand the _Search Engine Optimization_ section.

![Category settings added by the Canonical URL Extension](../images/extension/canonical-url/categories.png){ loading=lazy }

| FIELD         | DESCRIPTION |
| ------------- | ----------- |
| Canonical URL | The URL that is used as the canonical URL for this category. For example: <br> _https://cross-domain.com/category.html_ <br> Set a relative URL to use the URL of another category or entity within the current store view. For example: <br> _other-category.html_ |

### CMS Page

Open the CMS page in edit mode and expand the _Search Engine Optimization_ section.

![CMS Page settings added by the Canonical URL Extension](../images/extension/canonical-url/cms-pages.png){ loading=lazy }

| FIELD         | DESCRIPTION |
| ------------- | ----------- |
| Canonical URL | The URL that is used as the canonical URL for this CMS page. For example: <br> _https://cross-domain.com/cms-page-url-key_ <br> Set a relative URL to use the URL of another CMS page or entity within the current store view. For example: <br> _url-key-of-another-cms-page_ |
