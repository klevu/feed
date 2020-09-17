# Klevu Feed Format (beta)

**This is a beta feed format.**
Do not use unless you have been explicitly asked to by a Klevu team member.

Instead please use our existing feed format, which is detailed here: 
[Feed format for Custom stores](https://support.klevu.com/knowledgebase/feed-format-for-custom-stores/)

# XSD Schema

The [XSD Schema](./schema.xsd) contains the various rules and validation
aspects of the Klevu Feed Format. Please reference this file directly from your XML
Feed which you create, in order to assist you in the validation of your feed data.

You can see how to achieve this by referencing the XML Sample below.

```xml
<rss
    version="2.0"
    xsi:noNamespaceSchemaLocation="./schema.xsd"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
```

# XML Sample

The [XML Sample file](./sample.xml) contains a valid implementation of the
Klevu Feed Format, complete with inline comments to guide you through the integration process
and what to do with each element of the XML feed.

# Examples

Please also click here for some [Additional Examples](./examples)
which focus on specific scenarios to give you an idea of how to provide various
data to Klevu. These examples contain partial records, focusing on the particular
scenario being highlighted, so please cross-reference them with the XSD Schema.

# Not yet supported

Please note that the following features may be documented in the XSD and Sample XML,
but are not currently supported at this stage of the beta:

- **Custom Record Types**. For example ACME_RECIPE or ACME_SHOP.
Currently only KLEVU_PRODUCT, KLEVU_CATEGORY and KLEVU_CMS are supported.
- **Group-currency price fallback to the base additional currency**.
Please specify <price/> and <sale_price/> for all groups and currencies,
even if they do not differ for that particular group.
