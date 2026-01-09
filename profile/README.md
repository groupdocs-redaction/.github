<h1 align="center">GroupDocs.Redaction</h1>

<h3 align="center">Protect sensitive content in 30+ document formats with text, image, annotation, and metadata redaction APIs</h3>

<p align="center">
  <strong>GroupDocs.Redaction</strong> is an on-premise document redaction API that removes or masks private content across PDFs, Office files, images, and emails while keeping formats intact. Automate compliance-safe sharing by redacting text, pictures, comments, annotations, and hidden metadata with granular rules and rasterized outputs.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/redaction/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/redaction/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/redaction/family)
[![API](https://img.shields.io/badge/API-2865E0?style=for-the-badge&logo=html5&logoColor=white)](https://apireference.groupdocs.com/redaction/)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/redaction/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/redaction)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Redaction News & Updates
- Stay current with [GroupDocs.Redaction release notes](https://releases.groupdocs.com/redaction/) for fixes, performance updates, and platform compatibility improvements.

## Supported Platforms & Repository Groups

### .NET Document Redaction (C#, ASP.NET, Services)
High-performance on-premise redaction library for PDFs, Office documents, images, and emails with text, image, annotation, and metadata scrubbing.
- **GroupDocs.Redaction-for-.NET**: Core API for redaction rules, worksheet/column targeting, rasterized PDF output, and metadata cleanup.  
  Repo & examples: https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET/tree/master/Examples
- **Demos & Plugins**: Visual Studio add-in and sample projects for quick evaluation.  
  Repo: https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET/tree/master/Demos

```csharp
// Case-sensitive phrase redaction in DOCX
using (Redactor redactor = new Redactor(@"sample.docx"))
{
  redactor.Apply(new ExactPhraseRedaction("John Doe", true, new ReplacementOptions("[personal]")));
  redactor.Apply(new AnnotationRedaction("(?im:john)", "[redacted]"));
  redactor.Save();
}
```

### Node.js Document Redaction (Node.js via Java)
Use the Java engine from Node.js to redact PDF/Office/Images with regex and area rules.
- **GroupDocs.Redaction-for-Node.js-via-Java**: NPM package and sample project for Node.js workflows.  
  Repo: https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-Node.js-via-Java

```javascript
// Redact a phrase and an annotation string in PDF (Node.js via Java)
const {
  Redactor,
  ExactPhraseRedaction,
  AnnotationRedaction,
  ReplacementOptions
} = require('groupdocs-redaction');

const redactor = new Redactor('sample.pdf');
redactor.apply(new ExactPhraseRedaction('John Doe', true, new ReplacementOptions('[personal]')));
redactor.apply(new AnnotationRedaction('(?im:john)', '[redacted]'));
redactor.save();
```

### Python Document Redaction (Python via .NET)
Call the .NET engine from Python to automate redaction pipelines on Windows/Linux.
- **GroupDocs.Redaction-for-Python-via-.NET**: PyPI package with usage samples and CLI guides.  
  Repo: https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-Python-via-.NET

```python
# Redact a phrase and annotation text in DOCX (Python via .NET)
from groupdocs.redaction import Redactor, ExactPhraseRedaction, AnnotationRedaction, ReplacementOptions

with Redactor("sample.docx") as redactor:
    redactor.apply(ExactPhraseRedaction("John Doe", True, ReplacementOptions("[personal]")))
    redactor.apply(AnnotationRedaction("(?im:john)", "[redacted]"))
    redactor.save()
```

## Business Use-Cases
- PII/PHI removal for compliance-ready document sharing (GDPR, HIPAA, SOC2).
- Legal document production with targeted phrase and annotation cleanup.
- Financial statements and invoices with selective cell/column redaction.
- Email and PDF repository sanitization with metadata removal and audit logs.
- Government forms and permit packages requiring consistent redaction rules.

## API Key Features & Benefits
- 30+ formats: PDF, DOCX/DOTX, XLSX, PPTX, TIFF/PNG/JPG, MSG/EML, TXT/RTF, and more.
- Redaction types: text (case-sensitive/regex), image area overlay, annotation cleanup, metadata removal/replacement.
- Worksheet/column targeting for spreadsheets; preserve original format or export rasterized PDF for irreversible protection.
- Compliance-ready output: switch PDF/A compliance levels when saving as rasterized PDF.
- Cross-platform: build on Windows/Linux/macOS with .NET Framework 4.6.2+, .NET Core 3.1+, or .NET 6+.
- Performance-focused: batch rules, reusable configurations, and consistent results across repositories.

## Getting Started
- Install via NuGet: `Install-Package GroupDocs.Redaction` or `dotnet add package GroupDocs.Redaction`
- Clone samples: `git clone https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET.git`
- Open `Examples/GroupDocs.Redaction.Examples.CSharp.sln` in Visual Studio or run from CLI.
- Set license in `Constants.cs` or request a [temporary license](https://purchase.groupdocs.com/temporary-license) for full evaluation.
- Run examples and inspect outputs under `Examples/GroupDocs.Redaction.Examples.CSharp.Core/bin/Output`.

## Technical Support & Resources
- Documentation and tutorials: https://docs.groupdocs.com/redaction/
- Free support forum: https://forum.groupdocs.com/c/redaction
- Temporary license: https://purchase.groupdocs.com/temporary-license

## Tags
`document-redaction` `pdf-redaction` `office-redaction` `text-redaction` `image-redaction` `annotation-redaction` `metadata-cleanup` `pii-removal` `phi-protection` `compliance` `gdpr` `hipaa` `sox` `pii-masking` `pdf-sanitization` `document-security` `sensitive-data-protection` `rasterized-pdf` `regex-redaction` `spreadsheet-redaction` `email-redaction`
