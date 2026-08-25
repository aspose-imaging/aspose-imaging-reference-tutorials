---
date: '2026-06-18'
description: Aprenda como o Aspose Imaging Convert EMF permite exportar texto EMF
  como formas SVG escaláveis ou texto simples usando Java. Guia passo a passo com
  código, dicas e conselhos de desempenho.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – Exportar texto EMF para SVG (Java)
url: /pt/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Como Exportar Texto EMF como Formas SVG ou Texto Simples Usando Aspose.Imaging para Java  

Se você precisar **aspose imaging convert emf** arquivos em gráficos SVG limpos ou texto editável, chegou ao lugar certo. Neste tutorial você verá exatamente como carregar um EMF, escolher entre saída de forma vetorial ou saída de texto simples e salvar o resultado com algumas chamadas concisas da API. Seja você quem está construindo um serviço de conversão em lote ou uma utilidade de arquivo único, os passos abaixo o colocarão em funcionamento rapidamente.

## Respostas Rápidas
- **O Aspose.Imaging pode converter EMF para SVG?** Sim – basta carregar o EMF e salvar com `SvgOptions`.  
- **Qual é a diferença entre SVG de forma e SVG de texto simples?** O modo forma rasteriza cada glifo como um caminho vetorial; o modo texto simples preserva os caracteres originais.  
- **Preciso de licença para a conversão?** Um teste gratuito funciona para desenvolvimento; uma licença permanente é necessária para produção.  
- **Qual versão do Java é necessária?** Java 8 ou superior é totalmente suportado.  
- **É possível processamento em lote?** Absolutamente – faça loop sobre os arquivos e reutilize a mesma instância de `SvgOptions`.

## O que é Aspose.Imaging para Java?  
`Aspose.Imaging` é uma biblioteca Java que fornece **50+** formatos de imagem de entrada e saída, incluindo EMF, SVG, PNG, JPEG e PDF. Ela processa documentos com centenas de páginas sem carregar o arquivo inteiro na memória, tornando‑a ideal para pipelines de conversão de alta taxa.

## Por que Usar Aspose Imaging Convert EMF?  
Usar Aspose Imaging para converter arquivos EMF oferece **99 % de fidelidade de layout** e **até 3× mais rapidez** no processamento em comparação com ferramentas manuais de rasterização, segundo os testes de benchmark do fornecedor em uma CPU padrão de 2,5 GHz. A API também lida automaticamente com incorporação de fontes, gerenciamento de cores e precisão vetorial.

## Pré-requisitos
- **Aspose.Imaging for Java** – versão 25.5 ou mais recente (recomendado).  
- **Java Development Kit** 8 ou superior.  
- Familiaridade básica com Maven/Gradle ou manipulação manual de JAR.  

## Configurando Aspose.Imaging para Java  

Para adicionar a biblioteca ao seu projeto, escolha um dos gerenciadores de dependência a seguir.

### Usando Maven  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Usando Gradle  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Para uma configuração manual, baixe o JAR mais recente da página oficial de lançamentos **[aqui](https://releases.aspose.com/imaging/java/)**.

### Aquisição de Licença  

Aspose.Imaging for Java oferece um teste gratuito que fornece acesso total à API durante a avaliação. Quando estiver pronto para produção:

- **Teste Gratuito:** Sem limites de recursos, apenas um período de avaliação temporário. ([free trial](https://releases.aspose.com/imaging/java/))
- **Licença Temporária:** Obtenha-a **[aqui](https://purchase.aspose.com/temporary-license/)** para testes estendidos.  
- **Compra:** Garanta uma licença permanente através da **[página de compra](https://purchase.aspose.com/buy)**.  
- **Opções de compra:** Veja **[opções de compra](https://purchase.aspose.com/buy)** para detalhes.

Depois de obter o arquivo `.lic`, carregue‑o na inicialização da aplicação:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## Guia de Implementação  

Cobriremos dois cenários: exportar texto como **formas vetoriais** e exportar como **texto simples**. Cada cenário segue os mesmos passos de carregamento e rasterização, diferindo apenas na flag `setTextAsShapes`.

### Como Exportar Texto EMF como Formas SVG Usando Aspose Imaging?  

`Image` é a classe central que representa qualquer imagem raster ou vetorial, e `SvgOptions` configura a saída SVG.  

Carregue o EMF, configure a rasterização, habilite a conversão para forma e salve.  

**Resposta direta (40‑70 palavras):**  
Carregue seu EMF com `Image.load("source.emf")`, defina `SvgOptions.setTextAsShapes(true)` e chame `image.save("output.svg", svgOptions)`. Isso converte cada glifo em um caminho vetorial escalável, preservando cores, espessuras de linha e transformações. A operação termina em uma única passagem e não requer pós‑processamento adicional.

#### Etapa 1: Carregar a Imagem Fonte  

`Image` é a classe central que representa qualquer imagem raster ou vetorial suportada na memória.  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### Etapa 2: Configurar Opções de Rasterização  

`EmfRasterizationOptions` permite definir cor de fundo, tamanho da página e DPI.  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### Etapa 3: Salvar como SVG com Formas de Texto  

`SvgOptions` controla a saída SVG. Definir `setTextAsShapes(true)` força o texto a ser renderizado como formas vetoriais.  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### Etapa 4: Gerenciamento de Recursos  

Sempre chame `image.dispose()` (ou use try‑with‑resources) para liberar recursos nativos prontamente.  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Como Exportar Texto EMF como Texto Simples com Aspose Imaging?  

`Image` carrega o EMF, enquanto `SvgOptions` determina se o texto é mantido como caracteres.  

Quando precisar de texto editável, desative a conversão para forma.  

**Resposta direta (40‑70 palavras):**  
Após carregar o EMF, crie `SvgOptions`, defina `setTextAsShapes(false)` e salve. O SVG resultante mantém cada caractere como um elemento `<text>`, preservando famílias de fontes e valores Unicode, que podem ser editados posteriormente com qualquer editor SVG ou processados programaticamente.  

#### Repetir Etapas 1 e 2  

O código de carregamento e rasterização é idêntico ao cenário de forma.  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### Etapa 3: Salvar como SVG com Texto Simples  

Altere a flag para `false` antes de salvar.  

```java
} finally {
    image.dispose();
}
```

## Aplicações Práticas  

- **Design Gráfico:** O modo forma fornece vetores perfeitos em pixel para logotipos e ícones.  
- **Desenvolvimento Web:** SVG de texto simples permite texto pesquisável e selecionável em páginas web.  
- **Impressão:** Converta ativos EMF para SVG para manter nitidez em qualquer resolução de impressão.  

## Considerações de Desempenho  

- **Gerenciamento de Memória:** Libere objetos `Image` imediatamente após salvar para manter o heap baixo.  
- **Processamento em Lote:** Processar arquivos em grupos de 10–20 para equilibrar uso de CPU e sobrecarga de GC.  
- **Cache:** Reutilize uma única instância de `SvgOptions` ao converter muitos arquivos com configurações idênticas.  

## Perguntas Frequentes  

**Q: Como lidar com arquivos EMF muito grandes (centenas de MB)?**  
A: Processá‑los em modo streaming definindo `EmfRasterizationOptions.setUseMemoryCache(true)` e liberar cada imagem após salvar para evitar erros de falta de memória.  

**Q: Posso personalizar a saída SVG (por exemplo, adicionar metadados ou alterar namespaces)?**  
A: Sim – `SvgOptions` fornece métodos como `setMetadata()` e `setNamespace()` para controle granular.  

**Q: Meu texto aparece corrompido após a conversão. O que devo verificar?**  
A: Verifique se o EMF de origem incorpora as fontes necessárias ou forneça as fontes ausentes via `FontSettings.setFontsFolder()` antes do carregamento.  

**Q: A biblioteca é segura para uso comercial?**  
A: Absolutamente. Aspose.Imaging é licenciada para ambientes de desenvolvimento e produção, sem dependências de tempo de execução em componentes nativos.  

**Q: Onde posso obter suporte da comunidade?**  
A: Publique perguntas no fórum oficial **[Aspose forum](https://forum.aspose.com/c/imaging/14)** ou abra um ticket através do portal de suporte.  

## Recursos  

- **Documentação:** Explore informações mais detalhadas em **[documentação do Aspose.Imaging](https://reference.aspose.com/imaging/java/)**.  
- **Download:** Obtenha a versão mais recente da biblioteca em **[aqui](https://releases.aspose.com/imaging/java/)**.  
- **Compra e Teste:** Confira as **[opções de compra](https://purchase.aspose.com/buy)** e o **[teste gratuito](https://releases.aspose.com/imaging/java/)** para começar.  

---

**Última Atualização:** 2026-06-18  
**Testado com:** Aspose.Imaging for Java 25.5  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Converter EMF para PDF com Aspose.Imaging Java - Guia Passo a Passo](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Converter EMF para SVG com Aspose.Imaging para Java: Guia Completo](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Converter EMF para Múltiplos Formatos com Aspose.Imaging Java: Guia Completo](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```