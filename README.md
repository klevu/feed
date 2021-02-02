# Klevu Feed Format (Feed V2)

Please visit our support website for full documentation and answers to the most common questions:  
[https://support.klevu.com/knowledgebase/feed-format](https://support.klevu.com/knowledgebase/feed-format)

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

> :warning: **The following features are not yet supported**,
but are included in the XSD Schema and Sample XML file as they will be coming soon.

- **Magento group/tier prices are not currently supported**,
for example Wholesale or Retail pricing, where our Magento extension exports group prices in a
[particular format](https://support.klevu.com/knowledgebase/magento-group-prices-and-catalog-price-rules/).

# Need help?

Find answers to the most common questions on the Klevu Support website:  
[https://support.klevu.com/knowledgebase/feed-format](https://support.klevu.com/knowledgebase/feed-format)

If you still can't find what you're looking for, please contact Klevu Support (support@klevu.com).
