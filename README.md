# CLOUDFRONT WITH S3 BUCKET ORIGIN

> Content delivery with Amazon CloudFront.

A hands-on workshop from the [AWS First Cloud Journey](https://github.com/vanhoangkha/aws-first-cloud-journey) series, available in English and Vietnamese.

**Read the workshop online:** https://vanhoangkha.github.io/000094-Cloudfront/

## Overview

This hands-on lab will guide you through the steps to host static web content in an Amazon S3 bucket, protected and accelerated by Amazon CloudFront . Skills learned will help you secure your workloads in alignment with the AWS Well-Architected Framework.

## Workshop contents

1. Create S3 bucket
2. Upload example index.html file
3. Configure Amazon CloudFront
4. Tear Down

## Prerequisites

- An AWS account with permissions to create the resources used in the labs
- Basic familiarity with the AWS Management Console
- [Hugo](https://gohugo.io/installation/) (extended edition) if you want to run the site locally

## Run locally

```bash
git clone --recurse-submodules https://github.com/vanhoangkha/000094-Cloudfront.git
cd 000094-Cloudfront
hugo server
```

Then open http://localhost:1313 in your browser.

## Repository structure

| Path | Purpose |
| --- | --- |
| `content/` | Workshop pages (`*.md` English, `*.vi.md` Vietnamese) |
| `static/` | Images and other static assets |
| `layouts/` | Hugo layout overrides |
| `themes/` | Hugo theme |
| `config.toml` | Site configuration |

## Cost and cleanup

The labs create AWS resources that may incur charges. Delete the resources you created when you finish the workshop.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

To report a security issue, see [SECURITY.md](SECURITY.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
