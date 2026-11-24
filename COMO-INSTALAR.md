# Meu Cartão — como colocar no iPhone

O app é um "web app" (PWA): você hospeda os arquivos uma vez, grátis, e adiciona à Tela de Início do iPhone. Ele abre em tela cheia, como um app, e funciona sem internet. Os dados ficam só no seu iPhone.

## 1. Hospedar os arquivos (uma vez só, ~10 min)

**Opção recomendada: GitHub Pages (grátis e permanente)**

1. Crie uma conta em github.com (se ainda não tiver).
2. Clique em **New repository**, dê o nome `meu-cartao`, marque **Public** e crie.
3. Clique em **uploading an existing file** e arraste TODOS os arquivos desta pasta:
   `index.html`, `manifest.json`, `sw.js`, `icon-180.png`, `icon-192.png`, `icon-512.png`.
   Clique em **Commit changes**.
4. Vá em **Settings → Pages**. Em *Branch*, escolha `main` e `/ (root)` e salve.
5. Em 1–2 minutos o endereço fica pronto: `https://SEU-USUARIO.github.io/meu-cartao/`

(Alternativa sem GitHub: app.netlify.com/drop — arraste a pasta e ele gera um endereço.)

## 2. Instalar no iPhone

1. Abra o endereço no **Safari** do iPhone.
2. Toque em **Compartilhar** (quadrado com seta) → **Adicionar à Tela de Início** → Adicionar.
3. Abra pelo ícone "Cartão". Na primeira vez ele abre em **Ajustes**: informe o dia de fechamento e o de vencimento e toque em **Salvar**.

## 3. O dia a dia

- **Lançar** (tela inicial): digite o valor no teclado e toque na categoria. Pronto, salvo.
  Antes de tocar na categoria, você pode adicionar descrição, parcelas (o valor digitado é o total) ou outra data.
- **📷 Ler compra**: escolha o print da notificação do banco (ou uma foto do comprovante). O app lê o valor, a data, a loja e as parcelas e sugere a categoria. Você confere e toca em Salvar. Também dá para colar o texto da notificação.
  **Importar fatura fechada**: dentro de "Ler compra", envie o PDF da fatura (ou prints das páginas) e escolha de qual mês ela é. O app encontra as compras parceladas (ex.: "MAGAZINE LUIZA 05/10 189,90") e lança as parcelas que faltam nas próximas faturas. Você revisa a lista antes; se a fatura já foi importada, ele avisa. PDFs com senha pedem a senha do banco.
  A leitura é feita no próprio iPhone. Na primeira vez ele baixa o leitor (alguns MB), então é preciso internet. O app aprende a categoria de cada loja que você salva.
- **Fatura**: total, quanto falta para a meta, datas de abertura/fechamento/vencimento, gastos por categoria e lista de compras. Use ‹ › para navegar entre faturas. Toque numa compra para editar ou excluir.
  Para mudar as datas, use **Ajustar datas da fatura**: dá para alterar abertura, fechamento e vencimento. As novas datas ficam salvas e valem para esta fatura e as próximas; as faturas anteriores não mudam.
- **Resumo**: totais da fatura em aberto, da última fechada, de todas as fechadas e das próximas (parcelas já comprometidas), mais um gráfico de barras por fatura com a linha da meta. Toque numa barra para ver os detalhes, ou numa fatura da lista para abri-la.
- **Metas**: meta total por fatura e meta por categoria. O app avisa quando você passa de uma meta.
- **Ajustes**: dias do cartão, categorias (criar/remover) e **backup**.

## 4. Sobre o atalho (app Atalhos / Siri)

Importante: no iPhone, o app da Tela de Início guarda os dados separados do Safari. Um atalho do app Atalhos só consegue abrir links no Safari — então ele **não** alimenta o app da Tela de Início.

Por isso há dois jeitos de usar. Escolha **um**:

### Jeito A (recomendado): o próprio ícone é o atalho
O ícone "Cartão" já abre direto na tela de lançamento: toque no ícone → digite o valor → toque na categoria. São 3 toques, e é o jeito mais seguro para seus dados.

### Jeito B: atalho no app Atalhos (também funciona com "E aí Siri")
Neste jeito, **tudo** é usado pelo Safari (não instale na Tela de Início pelo passo 2).

1. Abra o app **Atalhos** → **+**.
2. Adicione **Pedir Entrada**: tipo *Número*, pergunta "Valor da compra?".
3. Adicione **Escolher da Lista**, com os itens: Mercado, Restaurantes, Delivery, Transporte, Combustível, Saúde, Casa, Lazer, Compras, Assinaturas, Viagem, Outros (os mesmos nomes das categorias do app).
4. Adicione **URL** com:
   `https://SEU-USUARIO.github.io/meu-cartao/?valor=`[Entrada Fornecida]`&cat=`[Item Escolhido]
   (insira as variáveis tocando nelas na barra acima do teclado)
5. Adicione **Abrir URLs**.
6. Dê o nome "Gasto" ao atalho. Nos detalhes, toque em **Adicionar à Tela de Início**.

Para ver a fatura, crie outro atalho com só **Abrir URLs**: `https://SEU-USUARIO.github.io/meu-cartao/?tela=fatura`

Parâmetros opcionais na URL: `&desc=Padaria` e `&parcelas=3`.

Atenção: o Safari pode apagar dados de sites que você não abre por algumas semanas. No Jeito B, faça backup com frequência.

## 5. Backup

Em **Ajustes → Exportar backup**, salve o arquivo no app Arquivos/iCloud Drive. Para restaurar, use **Importar backup**.
Se você trocar de iPhone ou apagar o ícone do app, os dados vão junto, a não ser que tenha um backup.

## Como a fatura é calculada

- Compras feitas **no dia do fechamento ou depois** entram na fatura seguinte.
- A fatura recebe o nome do mês do **vencimento** (como os bancos fazem).
- Compras parceladas: cada parcela cai em uma fatura; os centavos que sobram ficam na 1ª parcela.
