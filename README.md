# ObraFácil — nova versão

Aplicação web progressiva (PWA), em português de Portugal, para preparar orçamentos de construção civil num telemóvel ou computador.

## Funcionalidades
- Painel inicial e histórico de orçamentos.
- Dados do cliente e da obra, validade, desconto, IVA, notas e estado do orçamento.
- Serviços completos configuráveis (parede de blocos/tijolo, pintura, cerâmica, pladur, impermeabilização e telhado) com cálculo de área, desconto de vãos e etapas opcionais num único item.
- Catálogo de serviços por categoria, com preços de referência editáveis.
- Quantidades diretas e calculadoras de área, parede, volume e metro linear.
- Preço direto ou custo + margem, incluindo materiais, outros custos, horas, número de trabalhadores e ajudante.
- Orçamentos guardados localmente, edição, duplicação, estado, pesquisa e remoção.
- Documento de impressão que pode ser guardado em PDF pelo navegador.
- Partilha do resumo através da folha de partilha do dispositivo; o PDF é anexado manualmente depois de o guardar.
- Exportação/importação de cópia de segurança JSON.
- Manifesto PWA e service worker para instalação após publicação em HTTPS.

## Publicar no GitHub Pages
1. Descarregue e extraia o ZIP.
2. Envie os ficheiros da pasta para a raiz do repositório GitHub: `index.html`, `app.js`, `manifest.webmanifest`, `sw.js`, `icon.svg` e `README.md`.
3. Em Settings → Pages, escolha a branch `main` e a pasta `/(root)` e guarde.
4. Abra o URL Pages no Chrome e teste criar, guardar, reabrir, imprimir e exportar uma cópia.

## Dados e segurança
Os dados são guardados no armazenamento local do navegador e não são sincronizados entre dispositivos. Exportar uma cópia regularmente é essencial. A importação substitui os dados atuais e pede confirmação.

## Notas importantes
- Os preços iniciais são exemplos indicativos editáveis, não uma tabela oficial nem garantia de preço de mercado. Confirme se incluem materiais, mão de obra, transporte, desperdício e IVA.
- A taxa de IVA é configurável; confirme a taxa e o enquadramento fiscal aplicáveis a cada obra antes de entregar o orçamento.
- A aplicação foi verificada quanto à sintaxe JavaScript; é necessário testar as interações no navegador real e no GitHub Pages antes de utilização profissional.
