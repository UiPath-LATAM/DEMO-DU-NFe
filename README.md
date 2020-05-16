# DU-NFe
Demo de UiPath Document Understanding para Nota Fiscal NFe

### Descrição
- Utilizando o Extrator ML para Invoices na __Nota Fiscal Eletrônica__
- Utilizando o OCR __Microsoft Computer Vision__(Azure Cognitive Services)
    
### Pré-Requisitos
- Conta Community ou Enterprise no __UiPath Automation Cloud__
  - API Key do Serviço Document Understanding
- Activities Packages do repositório Official:
  - UiPath.UIAutomation.Activities
  - UiPath.System.Activities
  - UiPath.IntelligentOCR.Activities
  - UiPath.DocumentUnderstanding.ML.Activities (Extratores de ML)
  - *UiPath.OmniPage.Activities (Caso opte por usar este OCR free)*
  - *UiPath.OCR.Activities (Caso opte por usar o ScreenOCR UiPath)*

  
### Resultados
- __Nota Fiscal Eletrônica__(DANFE)
  - Consegue extrair mais de *90%* das informações.
  - Os dados de endereçamento são capturados com sucesso pelo ML, menos o *CEP*, por se tratar de um dado peculiar brasileiro       com sigla e formação diferente de muitos paises, neste caso pode-se complementar a extração usando o regex, form ou           intelligent form extractor
- __Nota Fiscal de Serviços__  
  - Já para as NF de Serviços consegue extrair pouca informação devido ao padrão diversificado.
  - Para este caso será preciso compor os extratores com ReGex e/ou Form e Intelligent Form, por se tratar de um
    um documento semi estruturado
