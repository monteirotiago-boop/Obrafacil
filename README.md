# ObraFácil V3 — Orçamentos de construção civil

Aplicação web móvel, em português de Portugal, para uso inicial num único dispositivo.

## Novidades V3
- Interface com categorias e fluxos de trabalho separados.
- Catálogo de serviços editável com preços-base indicativos.
- Construtor de parede/muro: área líquida, desconto de portas/janelas e seleção separada de assentamento, reboco em cada face e pintura em cada face.
- Calculadoras rápidas de pintura, pavimento, betão/escavação, pladur, telhado/impermeabilização e metros lineares.
- Orçamentos com dados do cliente, NIF/email opcionais, nome da obra, morada, data, validade, desconto, IVA e notas.
- Cálculo de preço direto ou custo + margem, com materiais, mão de obra, ajudante e outros custos.
- Orçamentos guardados com opções para abrir/editar, imprimir/guardar PDF, partilhar resumo, duplicar e apagar.
- Exportação/importação de cópia de segurança JSON.
- PWA básica e cache offline.

## Fórmulas principais
- Área = comprimento × largura ou comprimento × altura.
- Volume = comprimento × largura × profundidade.
- Parede líquida = comprimento × altura − área de portas − área de janelas, nunca abaixo de zero.
- Custo unitário = materiais + outros custos + (horas por unidade × custo horário da equipa).
- Preço por custo + margem = custo unitário × (1 + margem/100).
- Subtotal = soma de quantidade × preço unitário.
- Desconto limitado ao subtotal.
- IVA acrescentado = (subtotal − desconto) × taxa configurada.
- Quando os preços já incluem IVA, o IVA é discriminado sem aumentar o total.

A margem é uma percentagem sobre o custo (markup), não a margem bruta percentual sobre o preço final.

## Preços
Os preços do catálogo são referências de arranque, não uma tabela oficial de preços nem uma garantia de preço local. Variam com região, quantidades, acessos, estado do suporte, altura, preparação, materiais incluídos, resíduos, andaimes, equipamento e IVA. Algumas referências públicas agrupam materiais e mão de obra ou incluem várias etapas; não compare esses valores sem confirmar o âmbito. O assentamento de bloco tem um valor-base de trabalho editável, pois não foi encontrada uma tarifa pública nacional homogénea para mão de obra isolada. Confirme todos os preços com o responsável pela obra antes de enviar propostas.

## Dados e segurança
Os dados ficam no `localStorage` do navegador. Não existe sincronização na nuvem nem conta de utilizador. Limpar os dados do site pode apagar orçamentos; exporte cópias regularmente. A importação substitui os dados atuais. Não publique dados de clientes no repositório GitHub.

## Publicação no GitHub Pages
1. No repositório, substitua os ficheiros pelos desta versão: `index.html`, `app.js`, `manifest.webmanifest`, `sw.js`, `icon.svg` e `README.md`.
2. Mantenha GitHub Pages configurado para branch `main`, pasta `/(root)`.
3. Aguarde pela publicação e abra o URL do Pages.
4. No Samsung, abra no Chrome e use o menu ⋮ → “Instalar aplicação” ou “Adicionar ao ecrã principal”.

## PDF e WhatsApp
O botão de impressão abre a impressão do navegador; no Android, escolha “Guardar como PDF”. O botão de partilha envia o resumo através do menu de partilha. Para enviar o documento completo pelo WhatsApp, guarde o PDF e anexe-o à conversa.

## Verificações antes de uso real
Teste pelo menos um orçamento de parede, um orçamento de pintura e um orçamento com IVA; confirme preços, quantidades, materiais incluídos e regras fiscais antes de apresentar propostas a clientes.
