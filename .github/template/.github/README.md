# 🟡 Community Browser CDN Build – JavaScript SDK Client Package

This repository provides a **community-maintained, browser-ready distribution** of the npm module
[`@aws-sdk/{repoName}`](https://www.npmjs.com/package/@aws-sdk/{repoName}/v/{repoVersion}).

Refer to the links below for detailed documentation:
- All Services - [https://cloud-sdk-builds.github.io](https://cloud-sdk-builds.github.io/)
- @aws-sdk/{repoName} - [https://cloud-sdk-builds.github.io/?sdk={repoName}](https://cloud-sdk-builds.github.io/?sdk={repoName})
- @aws-sdk/{repoName} v{repoVersion} - [https://cloud-sdk-builds.github.io/?sdk={repoName}&version={repoVersion}](https://cloud-sdk-builds.github.io/?sdk={repoName}&version={repoVersion})

Each package is **automatically built and published to a CDN**, allowing developers to use the SDK client **directly in browsers** with **zero bundling or build steps**.

> ⚡ No build process required — import directly from a CDN and start using it immediately.

---

## ⚠️ Trademark & Affiliation Notice

This project is a **community-operated distribution** and is **not affiliated with, endorsed by, or sponsored by**
Amazon Web Services or the official SDK maintainers.

“AWS”, “Amazon Web Services”, and related marks are trademarks of their respective owners.
All original SDK source code remains licensed under its respective upstream license.

---

## 📦 Usage

You can use this package directly in the browser via **jsDelivr** using an **import map**.

### 📌 This Version

CDN URL

```text
https://cdn.jsdelivr.net/gh/{orgName}/{repoName}@{repoVersion}/index.min.mjs
```

SRI SHA Hash

```text
{SRI_SHA}
```

### 📌 Latest Version

CDN URL

```text
https://cdn.jsdelivr.net/gh/{orgName}/{repoName}/index.min.mjs
```

SRI SHA Hash

```
This SRI SHA Hash changes dynamically when there is any new version release so stop using latest build in production without mentioning version number in the url. So Use latest version by mentioning its version number in url with its SHA integrity.
```

---

## 🧩 Example (Browser Usage)

ImportMap

```html
<script type="importmap">
      {
        "imports": {
            "@aws-sdk/{repoName}": "https://cdn.jsdelivr.net/gh/{orgName}/{repoName}@{repoVersion}/index.min.mjs"
        },
          "integrity": {
            "https://cdn.jsdelivr.net/gh/{orgName}/{repoName}@{repoVersion}/index.min.mjs": "{SRI_SHA}"
        }
      }
</script>
```

Full Importmap Example

```html
<!DOCTYPE html>
<html lang="en">
      <head>
            <meta charset="utf-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <script type="importmap">
                  {
                    "imports": {
                        "@aws-sdk/{repoName}": "https://cdn.jsdelivr.net/gh/{orgName}/{repoName}@{repoVersion}/index.min.mjs"
                    },
                      "integrity": {
                        "https://cdn.jsdelivr.net/gh/{orgName}/{repoName}@{repoVersion}/index.min.mjs": "{SRI_SHA}"
                    }
                  }
            </script>
      </head>
      <body>
            <h1>Hello World!</h1>
            <script type="module">
                  import {  } from "@aws-sdk/{repoName}";
                  // Refer AWS SDK for JavaScript V3 - Service Documentation
            </script>
      </body>
</html>
```

---

## 📚 Available Packages

Any official `@aws-sdk/*` module published on npm can be built for browser CDN usage.

If a package you need is not yet available, please open an issue in:

```
https://github.com/{orgName}/.github/issues
```

---

## 🔧 Repository Contents

* **`index.min.mjs`**
  A single, production-ready, minified ES module bundle intended for direct browser usage.

* **`.github/`**
  Internal automation files (not required for end users).

* **`LICENSE`**
  Licensing terms for this distribution.

---

## 🌐 CDN URL Format

### Latest Version

```
https://cdn.jsdelivr.net/gh/{orgName}/{aws_service_name}/index.min.mjs
```

### Specific Version

```
https://cdn.jsdelivr.net/gh/{orgName}/{aws_service_name}@{aws_version}/index.min.mjs
```

Replace

- {aws_service_name} with client-s3 or client-dynamodb or client-lambda etc.,
- {aws_version} with aws service specific version

---

## 🔒 Security Notice

When using CDN builds in production environments:

* Always pin to a specific version (`@{repoVersion}`)
* Avoid using `latest` in production to prevent unexpected breaking changes

---

## 🤝 Contributing & Requests

To request support for additional browser-ready SDK packages, please open an issue:

```
https://github.com/{orgName}/.github/issues
```

---

## 📜 License

This distribution follows the license terms included in the repository:

```
https://github.com/{orgName}/{repoName}/blob/refs/tags/{repoVersion}/LICENSE
```

---
