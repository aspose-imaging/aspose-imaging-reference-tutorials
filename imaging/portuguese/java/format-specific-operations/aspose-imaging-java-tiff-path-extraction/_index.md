---
date: '2026-09-02'
description: Aprenda como criar um caminho de recorte e extraí-lo de imagens TIFF
  usando Aspose.Imaging para Java. Siga instruções passo a passo para converter TIFF
  em PSD de forma eficiente.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: Aprenda como criar um caminho de recorte e extraí-lo de imagens TIFF
  usando Aspose.Imaging para Java. Siga o código passo a passo para converter TIFF
  em PSD.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: Criar caminho de recorte em TIFF com Aspose.Imaging para Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: Criar caminho de recorte em TIFF com Aspose.Imaging para Java
url: /pt/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar caminho de recorte em TIFF com Aspose.Imaging para Java

Neste guia abrangente, você aprenderá **como criar um caminho de recorte** em um arquivo TIFF e como extrair caminhos existentes usando Aspose.Imaging para Java. Ao final, você poderá converter imagens TIFF em arquivos PSD totalmente editáveis, tornando-os prontos para o Photoshop ou qualquer editor que suporte vetores.

## Respostas rápidas
- **O que é um caminho de recorte?** Um contorno vetorial que define regiões transparentes e opacas de uma imagem.  
- **Posso extrair um caminho existente de um TIFF?** Sim – Aspose.Imaging pode ler recursos de caminho incorporados e salvá-los como PSD.  
- **Como adiciono um novo caminho de recorte?** Crie um `PathResource`, preencha‑o com registros vetoriais e atribua‑o ao quadro ativo da imagem.  
- **Preciso de uma licença para uso em produção?** É necessária uma licença válida do Aspose.Imaging para implantações comerciais.  
- **Qual versão do Java é necessária?** JDK 8 ou superior; a biblioteca funciona com Java 11, 17 e posteriores.

## O que é um caminho de recorte?
Um caminho de recorte é um contorno baseado em vetor que indica aos mecanismos de renderização quais partes de uma imagem devem ser exibidas ou ocultas. Ele é armazenado como um recurso de caminho dentro de arquivos TIFF ou PSD e pode ser editado no Adobe Photoshop.

## Por que converter TIFF para PSD?
Converter TIFF para PSD permite edição sem perdas de camadas, máscaras e caminhos de recorte. Aspose.Imaging suporta **mais de 50 formatos de entrada e saída** e pode processar TIFFs com centenas de páginas sem carregar o arquivo inteiro na memória, proporcionando conversão em lote de alto desempenho.

## Pré-requisitos
- **Java Development Kit (JDK)** 8 ou mais recente instalado.
- **Aspose.Imaging for Java** biblioteca (adicione via Maven, Gradle ou download direto).  
- Familiaridade básica com conceitos de programação Java.

## Como configurar Aspose.Imaging para Java
Antes de adicionar qualquer código, certifique‑se de que a biblioteca está corretamente referenciada no seu sistema de build e que você possui um arquivo de licença válido. Isso garante que a API funcione sem restrições de avaliação e que todos os recursos, incluindo a manipulação de caminhos, estejam disponíveis.

### Maven
Adicione a seguinte dependência ao seu arquivo `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Inclua esta linha no seu arquivo `build.gradle`:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Download direto
Download the latest version from [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

#### Aquisição de licença
1. **Teste gratuito** – comece com um teste de 30 dias.  
2. **Licença temporária** – obtenha uma na [temporary license page](https://purchase.aspose.com/temporary-license/).  
3. **Compra** – adquira uma licença completa no [Aspose's website](https://purchase.aspose.com/buy).

Depois de instalado e licenciado, inicialize o Aspose.Imaging em seu projeto:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## Como extrair caminho de recorte de um TIFF?
Extrair um caminho de recorte envolve carregar o TIFF, localizar quaisquer recursos de caminho incorporados e gravar esses recursos em um novo arquivo PSD. O processo lê os dados vetoriais diretamente da imagem de origem, preservando a precisão e evitando a conversão raster.

Carregue o TIFF, itere através de seus recursos de caminho e salve o resultado como um PSD. Esta operação lê os dados vetoriais incorporados e os grava em um novo arquivo em uma única passagem.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

Iterar pelos recursos de caminho no quadro ativo e coletá‑los:
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

Salvar a imagem com os caminhos extraídos em um novo arquivo PSD:
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## Como criar caminho de recorte em TIFF?
Criar um caminho de recorte requer a construção de um `PathResource` que descreva o contorno vetorial desejado, anexá‑lo ao quadro ativo do TIFF e, em seguida, salvar a imagem (ou uma cópia) como PSD para que o caminho seja mantido. Essa abordagem permite adicionar programaticamente máscaras vetoriais a arquivos raster.

PathResource representa um caminho vetorial armazenado dentro de um arquivo de imagem.  
Inicialize um novo `PathResource` com os atributos necessários:
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

Atribua o recurso de caminho criado ao quadro ativo da imagem:
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

Salve o TIFF modificado como um PSD que agora contém o caminho de recorte:
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## Métodos auxiliares

### Criar registros
Gerar registros de caminho vetorial usando nós Bezier e registros de comprimento:
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### Criar registros Bezier
Converter arrays de coordenadas em registros de caminho vetorial Bezier:
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### Criar registro Bezier
Definir um único registro de caminho vetorial de nó Bezier:
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## Aplicações práticas
1. **Fluxos de trabalho de design gráfico** – Converta TIFF para PSD para editar camadas e máscaras no Photoshop.  
2. **Pipelines de imagem automatizados** – Processar em lote milhares de TIFFs, extraindo ou adicionando caminhos em tempo real.  
3. **Visualizações orientadas a dados** – Use caminhos vetoriais para gerar gráficos ou esquemas precisos a partir de fontes raster.

## Considerações de desempenho
- **Gerenciamento de memória** – Use try‑with‑resources para garantir que os objetos de imagem sejam descartados prontamente.  
- **Processamento em lote** – Paralelize as conversões com o `ForkJoinPool` do Java para grandes conjuntos de imagens.  
- **Manipulação de resolução** – Ajuste o DPI somente quando necessário para manter o tempo de processamento baixo enquanto preserva a qualidade.

## Conclusão
Agora você sabe como **criar caminho de recorte** em arquivos TIFF e extrair caminhos existentes usando Aspose.Imaging para Java. Essas técnicas permitem integrar manipulação avançada de imagens em qualquer fluxo de trabalho baseado em Java, desde utilitários de desktop até pipelines de processamento de nível empresarial.

### Próximos passos
- Experimente diferentes formas vetoriais e atributos de caminho.  
- Explore recursos adicionais do Aspose.Imaging, como marca d'água, conversão de formatos e manipulação de metadados.

## Perguntas frequentes

**Q: Posso usar Aspose.Imaging para Java em uma aplicação comercial?**  
A: Sim, desde que você possua uma licença comercial válida; um teste gratuito está disponível para avaliação.

**Q: Quais formatos de imagem o Aspose.Imaging suporta?**  
A: A biblioteca suporta mais de 100 formatos, incluindo TIFF, PSD, BMP, JPEG, PNG e muitos outros.

**Q: Como solucionar erros de extração de caminho?**  
A: Verifique se o TIFF de origem realmente contém recursos de caminho vetoriais; use a verificação `hasPathResources()` antes da extração.

**Q: É possível processar vários TIFFs em lote?**  
A: Absolutamente – combine o código de extração com streams paralelos do Java ou um serviço executor para lidar eficientemente com muitos arquivos.

**Q: Existem limitações ao criar caminhos de recorte em TIFF?**  
A: Formas complexas podem precisar de ajuste manual após a criação; a API lida de forma confiável com curvas Bezier padrão e linhas retas.

---

**Última atualização:** 2026-09-02  
**Testado com:** Aspose.Imaging for Java 24.12  
**Autor:** Aspose  

## Recursos

- [Documentação do Aspose.Imaging](https://reference.aspose.com/imaging/java/)
- [Download do Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/)
- [Comprar licença](https://purchase.aspose.com/buy)
- [Teste gratuito](https://releases.aspose.com/imaging/java/)
- [Licença temporária](https://purchase.aspose.com/temporary-license/)
- [Fórum de suporte da Aspose](https://forum.aspose.com/c/imaging/14)

## Tutoriais relacionados

- [Converter imagem para PSD com Aspose.Imaging para Java – Guia passo a passo](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [Como converter TIFF para GraphicsPath com Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [Carregar e salvar imagens TIFF eficientemente em Java com Aspose.Imaging](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}