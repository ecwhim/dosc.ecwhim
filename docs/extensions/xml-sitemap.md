# XML Sitemap

In addition to its settings, the [Magento 2 XML Sitemap Extension](https://www.ecwhim.com/magento-2-xml-sitemap-extension.html)
also uses the basic Magento settings for the XML sitemap (Stores > Configuration > Catalog > XML Sitemap).

## Configuration

Stores > Configuration > ECWHIM SEO > Sitemap > XML Sitemap

![Configuring the XML Sitemap Extension](../images/extension/xml-sitemap/configuration.png){ loading=lazy }

| FIELD                           | DESCRIPTION |
| ------------------------------- | ----------- |
| Exclude "Out of Stock" Products | Allows you to exclude from the sitemap information about the pages of products that are out of stock. Options: Yes/No |
| Source of Product Images        | Determines the source of product images for the sitemap. Options: Cache/Original |
| Add Product Videos              | Determines whether to include product videos in the sitemap. Options: Yes/No |
| Add Category Images             | Determines whether to include category images in the sitemap. Options: Yes/No |

## Manage sitemaps

Marketing > SEO & Search > Sitemap (Ecwhim SEO)

![Sitemap grid](../images/extension/xml-sitemap/grid.png){ loading=lazy }

### Create a new sitemap
Click `Add Sitemap` to go to the sitemap creation page.

![New sitemap](../images/extension/xml-sitemap/new-sitemap.png){ loading=lazy }

| FIELD                           | DESCRIPTION |
| ------------------------------- | ----------- |
| Filename    | The file name of the XML sitemap. For example: _sitemap.xml_ |
| Path        | Determines where the sitemap file is to reside on the server. Make sure that the path is writeable. For example: <br> `/` - Places the sitemap file at the base path. <br> `/sitemap/` - Places the sitemap file in a directory called _sitemap_. |
| Store View  | The store view where the sitemap applies. |
| Type        | Determines the sitemap type. Options: <br> **Default** - Combines information about pages of all entity types in the sitemap. <br> **Separated** - Creates a separate sitemap for each selected entity type. The suffix corresponding to the entity type will be added to the file name. For example: _sitemap_product.xml_ <br> **Composite** - Combines information about the pages of the selected entity types in the sitemap. |
| Entity Type | Determines the types of entities whose page information should be added to the sitemap. |

## CLI commands

1. Log in to your Magento server as, or switch to, the file system owner.
2. Navigate to your Magento project directory.

### View a list of sitemaps
To view a list of all sitemaps:
```shell
php bin/magento ecwhim-seo:xmlsitemap:list
```

### Generate sitemap(s)
Use this command to generate all or selected sitemaps.

Command options:
```shell
php bin/magento ecwhim-seo:xmlsitemap:generate [sitemap_id]
```
Where `[sitemap_id]` is a space-separated list of sitemap ids. Omit `[sitemap_id]` to generate all sitemaps.

### Delete sitemap(s)
Use this command to delete all or selected sitemaps.

Command options:
```shell
php bin/magento ecwhim-seo:xmlsitemap:delete [sitemap_id]
```
Where `[sitemap_id]` is a space-separated list of sitemap ids. Omit `[sitemap_id]` to delete all sitemaps.
