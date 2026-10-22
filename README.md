# Giorgio by Autotelic

<img src="https://giorgiobm.com/icon-512.png" width="72" height="72" alt="Giorgio">

**Ideas in motion. / Ideias em movimento.**

AI for research, coding, and everyday project work.

[Official website](https://giorgiobm.com/) · [About Giorgio](https://giorgiobm.com/about) · [Documentation](https://giorgiobm.com/docs) · [Giorgio Code](https://giorgiobm.com/docs/code) · [Giorgio Learn](https://giorgiobm.com/learn)

Giorgio brings together conversations, research, coding, and project context. Its Code workspace focuses on programming tasks, while Learn provides publicly readable educational material about AI systems.

## Three paths to get started

- **Investigate:** research a question and check original sources. [Research guide](https://giorgiobm.com/guides/pesquisar-com-fontes).
- **Build:** describe a reproducible coding problem and verify the change. [Coding guide](https://giorgiobm.com/guides/programar-com-ia).
- **Organize:** keep the goals, files, and instructions of a project together. [Project documentation](https://giorgiobm.com/docs/projects).

Product features, access requirements, and limits vary by plan and selected option. Check the [current plans](https://giorgiobm.com/plans) and [AI transparency page](https://giorgiobm.com/ai-transparency). AI-generated responses can contain mistakes; verify sources and code.

## Public discovery for agents

The website provides a read-only catalog of public product information and canonical URLs. It requires no authentication and exposes no accounts, private conversations, files, or inference operations.

[OpenAPI](https://giorgiobm.com/openapi.json) · [llms.txt](https://giorgiobm.com/llms.txt) · [Sitemap](https://giorgiobm.com/sitemap.xml)

### Command line

```sh
curl https://giorgiobm.com/api/public/site
curl -H "Accept: text/markdown" https://giorgiobm.com/about
```

### Python: read the public catalog

```python
import json
from urllib.request import Request, urlopen

request = Request("https://giorgiobm.com/api/public/site",
                  headers={"Accept": "application/json"})
with urlopen(request, timeout=30) as response:
    site = json.load(response)
print(site["name"], site["description"])
for page in site["pages"]:
    print(page["title"], page["url"])
```

### JavaScript: read the public catalog

```js
const response = await fetch("https://giorgiobm.com/api/public/site", {
  headers: {Accept: "application/json"},
  signal: AbortSignal.timeout(30000),
});
if (!response.ok) throw new Error(`HTTP ${response.status}`);
const site = await response.json();
console.log(site.name, site.description);
for (const page of site.pages) console.log(page.title, page.url);
```

These are public discovery examples, not inference SDKs.

## Em português

O Giorgio by Autotelic reúne conversa com IA, pesquisa, programação e contexto de projetos. Escolha uma tarefa concreta, forneça o contexto necessário e confira a entrega. Comece pelos [exemplos de uso](https://giorgiobm.com/use-cases) ou pelo [conteúdo aberto do Learn](https://giorgiobm.com/learn).

## Contact and public information

[Press information and brand assets](https://giorgiobm.com/press) · [Contact](https://giorgiobm.com/contact) · [Privacy](https://giorgiobm.com/privacy)

Public support address: support@giorgiobm.com.

This repository contains public product information and discovery examples. It does not contain the application's private source code or model weights.
