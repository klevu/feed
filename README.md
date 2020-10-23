# Klevu Feed Format (FeedV2)

**October 2020:** This is our new Klevu XML Feed Format, also known as *FeedV2*.
It is currently in **beta** as we carefully monitor all new submissions,
but has been tested thoroughly and is ready for public use.

# Integration Steps

The Klevu Feed is a method of providing your store data to be synced with Klevu.
You will host an XML file and keep it up to date as your catalog changes.
Klevu will then download this XML file from time to time
in order to update the search results that your customers see.

## 1. Download the XML Sample

The best way to get started is to download our sample file and begin populating with
your own data. The [XML Sample file](./sample.xml) contains a valid implementation
of the Klevu Feed Format, complete with inline comments to guide you through the
integration process and what to do with each element of the XML feed.

## 2. Verify against the XSD Schema

The [XSD Schema](./schema.xsd) contains the various rules and validation aspects
of the Klevu Feed format. Please reference this XSD directly from your XML file
to assist you in the validation of your feed data.

You can see how to achieve this by referencing the XML Sample above.

```xml
<rss
    version="2.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/klevu/feed/2.0/schema.xsd">
```

## 3. Host your XML file

Finally host your XML file in a publicly accessible location, and share the URL with Klevu
Support (support@klevu.com), who will configure our monitoring service to come and download
the feed from time to time.

That's it!

# Examples & Use Cases

You can also find some additional [Examples](./examples) which focus on specific
scenarios to give you an idea of how to provide various data to Klevu.

> :warning: **Please note that these examples contain partial data**, focusing only 
on the particular scenario being highlighted. For example some of them do not include required
fields such as &lt;id/&gt;, so please cross-reference them with the XSD Schema.

# Not yet supported

As mentioned at the top of this document, the Klevu Feed is in beta phase, and while we are making
our best efforts to ensure all of the information provided is accurate, there may be some discrepancies.

> :warning: **The following features are not yet supported**, but are included in the XSD Schema and
Sample XML file as they may be coming soon as part of the beta period.

- **Custom Record Types are not supported**, for example ACME_RECIPE or ACME_SHOP.
Currently only KLEVU_PRODUCT, KLEVU_CATEGORY and KLEVU_CMS are supported.
- **Group-currency price fallback to the base additional currency is not supported**.
Please specify &lt;price/&gt; and &lt;sale_price/&gt; for all groups and currencies,
even if they do not differ for that particular group.
