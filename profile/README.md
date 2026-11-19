<h1 align="center">GroupDocs.Redaction</h1>

<h3 align="center">Remove sensitive data from 40+ document and image formats with text, image, metadata, annotation and page redaction APIs</h3>

<p align="center">
  <strong>GroupDocs.Redaction</strong> is an on-premise document redaction API that permanently removes private content from PDF, Word, Excel, PowerPoint, OpenDocument, image, HTML and text files while keeping their formats intact. Redact text by exact phrase or regular expression, text in scans through the OCR engine of your choice, metadata, comments, and areas of images and pages, then save the result in its own format or as a rasterized PDF from which nothing can be recovered.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/redaction/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/redaction/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/redaction/family)
[![API](https://img.shields.io/badge/API-2865E0?style=for-the-badge&logo=html5&logoColor=white)](https://reference.groupdocs.com/redaction/)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/redaction/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/redaction)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Redaction News & Updates
* **NEW:** Released [GroupDocs.Redaction for Python via .NET 26.11](https://releases.groupdocs.com/redaction/python-net/release-notes/) on [PyPI](https://pypi.org/project/groupdocs-redaction-net/), on the 26.10 engine and .NET 10: rasterized PDF output and image-area redaction now work on Linux and macOS with no `libgdiplus`, and OCR connectors, page previews, redaction callbacks and loggers are Python objects and functions.
* Released [GroupDocs.Redaction.Mcp 26.9](https://www.nuget.org/packages/GroupDocs.Redaction.Mcp), an MCP server that lets AI agents (Claude, Cursor, GitHub Copilot) redact documents **locally**: files never leave your machine. [Get started](https://docs.groupdocs.com/redaction/mcp/).
* Published [GroupDocs.Redaction 26.10](https://www.nuget.org/packages/GroupDocs.Redaction/) for .NET on NuGet: builds for .NET 6, 8 and 10 on Windows, an evaluation mode of 25 documents per process, and patched cryptography packages.
* Published GroupDocs.Redaction 26.10 for [Java](https://releases.groupdocs.com/java/repo/com/groupdocs/groupdocs-redaction/26.10/) and for [Node.js via Java](https://www.npmjs.com/package/@groupdocs/groupdocs.redaction): OOXML compliance for Word documents, XLT, XLTX, XLTM and TAB spreadsheets, and custom handlers for page-area redaction.

## Supported Platforms & Repository Groups

### .NET Document Redaction (C#, ASP.NET, Services)
High-performance on-premise redaction for PDF, Office, OpenDocument and image files, with text, image, annotation, metadata and page redaction. `dotnet add package GroupDocs.Redaction`
* **[GroupDocs.Redaction-for-.NET](https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET)**: Core API examples for redaction rules, worksheet and column targeting, OCR connectors, rasterized PDF output and metadata cleanup.
* **[sample-windows-specific-redaction](https://github.com/groupdocs-redaction/sample-windows-specific-redaction)** and **[sample-crossplatform-redaction-docker-linux](https://github.com/groupdocs-redaction/sample-crossplatform-redaction-docker-linux)**: The Windows and the cross-platform engine, side by side.

```csharp
// Redact a customer's name and remove the comments of a Word document
using (Redactor redactor = new Redactor("sample.docx"))
{
    redactor.Apply(new ExactPhraseRedaction("Emily Johnson", new ReplacementOptions("[personal]")));
    redactor.Apply(new DeleteAnnotationRedaction());
    redactor.Save();
}
```

### Java Document Redaction (Maven, Spring Boot)
Native Java library with the same redactions, from the [GroupDocs Maven repository](https://releases.groupdocs.com/java/repo/): `com.groupdocs:groupdocs-redaction:26.11`.
* **[GroupDocs.Redaction-for-Java](https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-Java)**: Runnable Java examples for every redaction type.

```java
// Black out account numbers in a PDF
final Redactor redactor = new Redactor("statement.pdf");
try {
    redactor.apply(new RegexRedaction("\\d{2}\\s*\\d{2}[^\\d]*\\d{6}", new ReplacementOptions("[account]")));
    redactor.save();
} finally {
    redactor.close();
}
```

### Node.js Document Redaction (Node.js via Java)
The Java engine from Node.js. `npm install @groupdocs/groupdocs.redaction`
* **[GroupDocs.Redaction-for-Node.js-via-Java](https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-Node.js-via-Java)**: Runnable Node.js examples.

```javascript
// Black out account numbers in a PDF (Node.js via Java)
import { Redactor } from '@groupdocs/groupdocs.redaction'
import java from 'java'

const RegexRedaction = java.import('com.groupdocs.redaction.redactions.RegexRedaction')
const ReplacementOptions = java.import('com.groupdocs.redaction.redactions.ReplacementOptions')

const redactor = new Redactor('statement.pdf')
try {
  redactor.apply(new RegexRedaction('\\d{2}\\s*\\d{2}[^\\d]*\\d{6}', new ReplacementOptions('[account]')))
  redactor.save()
} finally {
  redactor.close()
}
```

### Python Document Redaction (Python via .NET)
The .NET engine from Python 3.5 to 3.14, on Windows, Linux and macOS, with the runtime embedded. `pip install groupdocs-redaction-net`
* **[GroupDocs.Redaction-for-Python-via-.NET](https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-Python-via-.NET)**: Runnable Python examples for every documented scenario.
* [PyPI](https://pypi.org/project/groupdocs-redaction-net/) · [Docs](https://docs.groupdocs.com/redaction/python-net/) · [API reference](https://reference.groupdocs.com/redaction/python-net/) · [Releases](https://releases.groupdocs.com/redaction/python-net/)

```python
# Redact a name and erase the metadata of a document (Python via .NET)
from groupdocs.redaction import Redactor
from groupdocs.redaction.redactions import EraseMetadataRedaction, ExactPhraseRedaction, MetadataFilters, ReplacementOptions

with Redactor("sample.docx") as redactor:
    redactor.apply(ExactPhraseRedaction("Emily Johnson", ReplacementOptions("[personal]")))
    redactor.apply(EraseMetadataRedaction(MetadataFilters.ALL))
    redactor.save()
```

### MCP Server for AI Agents (Claude, Cursor, Copilot)
Let AI agents redact documents through the GroupDocs engine, **locally over MCP**: no uploads, no cloud; it runs in evaluation mode out of the box and with your existing license.
* **[GroupDocs.Redaction.Mcp](https://github.com/groupdocs-redaction/GroupDocs.Redaction.Mcp)**: The MCP server, with one-click IDE install buttons and a NuGet tool.
* **[GroupDocs.Mcp.Installer](https://github.com/groupdocs/GroupDocs.Mcp.Installer)**: Cross-platform installer, per-client registration and post-install verification.
* **[GroupDocs.Redaction.Mcp.Tests](https://github.com/groupdocs-redaction/GroupDocs.Redaction.Mcp.Tests)**: Integration suite that verifies every published release.

```bash
# Install and run in one command (.NET 10), then just ask your agent:
dnx GroupDocs.Redaction.Mcp --yes
```

> "Redact every phone number and e-mail address in contract.pdf."
> "Remove the comments and the author from report.docx before I send it."

📘 [MCP documentation](https://docs.groupdocs.com/redaction/mcp/) · 📦 [NuGet](https://www.nuget.org/packages/GroupDocs.Redaction.Mcp)

### Business Use-Cases
* **PII and PHI removal:** Share compliance-ready documents (GDPR, HIPAA, CCPA).
* **Legal production:** Redact privileged phrases and comments across a production set.
* **Financial documents:** Remove account numbers from statements and invoices, cell by cell or column by column.
* **Scanned records:** Redact names in scanned forms through your OCR engine.
* **Publishing:** Erase authors, companies and other hidden metadata before release.

---

## ✅ API Key Features & Benefits
* **40+ formats**: PDF, DOCX, DOC, RTF, ODT, XLSX, XLS, ODS, CSV, PPTX, PPT, ODP, JPEG, PNG, TIFF, WEBP, HTML, Markdown and more.
* **Text redaction**: Exact phrases, case-sensitive or not, and regular expressions, replaced with text or covered with a box.
* **Text in images**: Scans and embedded images through an OCR connector, such as Tesseract.
* **Metadata, comments and pages**: Erase or rewrite properties, delete or rewrite annotations, remove pages.
* **Image and page areas**: Cover regions of images and pages.
* **Irreversible output**: Rasterize the result to PDF, with PDF/A compliance.
* **Policies and review**: Reusable redaction policies, and a callback that approves or rejects each match.

## 🆘 Technical Support & Resources
* **Documentation:** Full guides and tutorials at [docs.groupdocs.com/redaction](https://docs.groupdocs.com/redaction/).
* **Support:** Expert help at the [GroupDocs Free Support Forum](https://forum.groupdocs.com/c/redaction).
* **Evaluation:** Get a [Temporary License](https://purchase.groupdocs.com/temporary-license) for full feature testing.
* **Live Demo:** Try redaction online at [GroupDocs.Redaction apps](https://products.groupdocs.app/redaction/family).

## 🏷️ Tags

`python` `mcp` `mcp-server` `ai-agents` `document-redaction` `redaction-api` `pdf-redaction` `docx-redaction` `excel-redaction` `image-redaction` `ocr-redaction` `metadata-removal` `pii-removal` `gdpr` `hipaa` `data-sanitization` `rasterized-pdf` `on-premise` `dotnet` `java` `nodejs`
