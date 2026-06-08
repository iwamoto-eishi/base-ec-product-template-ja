# CSV Validation Policy

This document describes the basic checks that should be used when reviewing CSV files in this repository.

The goal is to keep examples useful for small retail stores while avoiding secrets, private store data, and real product information.

## Required Columns

CSV files should use the shared product listing columns:

```text
product_name,brand,category,color_name,jan,selling_price,stock,msrp,image_file,image_source_url,image_usage_status,seo_keywords,seo_description,notes
```

Before adding or updating a CSV file, check that:

- All required columns are present.
- The column order matches the template when possible.
- Each row has the same number of fields as the header.
- Blank values are intentional and explained in `notes` when needed.

## Fictional Sample Data Only

Public examples must use fictional data only.

- Use fictional product names.
- Use fictional brand names.
- Do not use real manufacturer names.
- Do not use real product URLs.
- Do not include private store notes, supplier details, order data, or cost data.

## JAN Values

Example CSV files should not use real JAN codes.

Recommended public example format:

```text
SAMPLE-JAN-0001
```

Avoid 13-digit numeric values in examples because they may look like real JAN codes.

## Image Source URLs

Image source fields should be safe placeholders unless the image rights are already confirmed.

- Use `example.invalid` for placeholder URLs.
- Do not use real product image URLs in fictional examples.
- Mark image usage status clearly, such as `confirmed`, `needs-check`, or `not-used`.
- Do not publish images or URLs when usage rights are unclear.

## SEO Fields

SEO fields should help store operators prepare clear customer-facing text.

- Keep SEO keywords relevant to the fictional product.
- Keep SEO descriptions short and natural.
- Avoid keyword stuffing.
- Avoid claims that cannot be verified from the sample data.

## Secrets And Private Data

CSV files must not include:

- API keys or tokens
- `.env` values
- Customer names or contact details
- Order data
- Private store settings
- Cost data or private supplier information
- Production BASE or Cloudinary information

## Review Checklist

- [ ] Required columns are present.
- [ ] Each row has the same number of fields as the header.
- [ ] Sample products are fictional.
- [ ] JAN values are clearly fictional.
- [ ] Image URLs are placeholders or rights-confirmed.
- [ ] SEO descriptions are short and customer-facing.
- [ ] No secrets or private store data are included.
