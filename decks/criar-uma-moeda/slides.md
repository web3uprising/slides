---
title: Criar uma moeda
description: Workshop WEB3UP x ACM FEUP. Desenhar, lançar e pagar um fino com uma moeda própria na Polkadot Hub TestNet.
---

<!-- .slide: class="hero" -->

<div class="eyebrow">workshop · acm feup</div>

# Criar uma<br><em>moeda</em>

<p class="lead">Web 3.0, uma nova versão da internet.</p>

<div class="pills">
  <span class="primary">14 OUT · 15:00</span>
  <span>até 16:30</span>
  <span>sala B340, FEUP</span>
</div>

Note:

Boas-vindas. Apresentar a WEB3UP e quem está a dar o workshop.
Pedir já a toda a gente que tenha o telemóvel com bateria e o portátil aberto.

---

## Hoje

<div class="steps">
  <div><i>1</i> Desenhar a moeda: supply, inflação, taxas</div>
  <div><i>2</i> Lançar a moeda numa plataforma</div>
  <div><i>3</i> Pagar um fino num terminal de pagamento</div>
</div>

<p class="muted" style="margin-top:48px">Moedas de teste. Não valem dinheiro. Podes partir tudo.</p>

Note:

Três passos, 90 minutos. No fim, cada equipa tem uma moeda a circular na sala.

---

## A agenda

| Hora | O quê |
|---|---|
| 15:00 | porquê uma moeda |
| 15:10 | desenhar a moeda |
| 15:35 | lançar a moeda |
| 16:00 | pagar com ela no terminal |
| 16:20 | o que correu mal |

---

<!-- .slide: class="hero" -->

<div class="eyebrow">parte 0 · 10 min</div>

## Porquê uma <em>moeda</em>?

---

## O banco que ninguém usava

- Abro um banco digital. Envias-me dinheiro, eu guardo, devolvo quando pedires.
- Ninguém confia. Publico o código. Faço auditorias. Reescrevo tudo em Rust.
- Continua sem clientes.
- Registo o banco no Banco de Portugal. **De repente toda a gente confia.**

Note:

Adaptado da abertura da Polkadot Blockchain Academy.
A pergunta para a sala: porque é que confiamos no nosso banco? Quase ninguém sabe o que o código faz.
Confiamos porque há uma autoridade que nos protege se o banco se portar mal.

---v

## Duas formas de confiar

<div class="cols">
  <div class="card">
    <h3>Autoridade</h3>
    <p>Um banco guarda o registo de quem tem quanto. Confias nele porque há regras, tribunais e polícia.</p>
  </div>
  <div class="card">
    <h3>Matemática</h3>
    <p>Milhares de computadores guardam o mesmo registo. Ninguém o muda sozinho. Confias porque podes verificar.</p>
  </div>
</div>

> Uma blockchain é um registo partilhado que ninguém controla sozinho.

---v

## Web 1, 2 e 3

<div class="cols" style="--n:3">
  <div class="card">
    <h3>Web 1</h3>
    <p><strong>ler.</strong> Páginas estáticas. Quem publica é quem tem um servidor.</p>
  </div>
  <div class="card">
    <h3>Web 2</h3>
    <p><strong>ler e escrever.</strong> Redes sociais. Tu crias, a plataforma fica com os dados e as regras.</p>
  </div>
  <div class="card">
    <h3>Web 3</h3>
    <p><strong>ler, escrever e possuir.</strong> O que é teu fica numa rede pública. A tua chave prova que é teu.</p>
  </div>
</div>

Note:

Uma moeda é o exemplo mais simples de "possuir" na internet. Por isso começamos por aqui.

---v

## Onde vamos trabalhar

<div class="cols">
  <div>
    <ul>
      <li><strong>Polkadot Hub TestNet</strong>, a rede de teste da Polkadot</li>
      <li>um bloco novo a cada <em>2,4 segundos</em></li>
      <li><strong>PAS</strong> é a moeda da rede. Paga o trabalho de cada transação (gás)</li>
      <li>aceita contratos em Solidity, como a Ethereum</li>
    </ul>
  </div>
  <div class="card">
    <h3>A tua carteira</h3>
    <p>Uma chave privada guardada no teu telemóvel. Quem tem a chave assina as transações e manda nas moedas.</p>
  </div>
</div>

---

## Abre a carteira

1. Abre o link da carteira no telemóvel.
2. Toca em **Receber** e mostra o código à organização.
3. Vais receber **1 PAS** para pagar o gás de hoje.

<p class="muted">A chave fica só no teu browser. Se limpares o browser, perdes a carteira. Usa Cópia para a guardar.</p>

Note:

Enquanto as pessoas abrem a carteira, a organização envia PAS a cada endereço.
Isto demora: começar logo e seguir com a parte 1 em paralelo.

---

<!-- .slide: class="hero" -->

<div class="eyebrow">parte 1 · 25 min</div>

## Desenhar a <em>moeda</em>

---

## Seis decisões

| Decisão | Pergunta |
|---|---|
| nome e símbolo | como se chama? `FINO`? `FEUP`? |
| quantidade inicial | quantas moedas existem no dia 1? |
| máximo | pode haver mais no futuro? |
| inflação | quanto cresce por ano, e quem recebe? |
| taxa | quanto custa cada pagamento, e para quem vai? |
| dono | quem pode emitir mais? |

---v

## Escassez ou inflação

<div class="cols">
  <div class="card">
    <h3>Máximo fixo</h3>
    <p>Como a Bitcoin. Ninguém imprime mais. Se a procura sobe, o preço sobe. Quem chegou primeiro ganha.</p>
  </div>
  <div class="card">
    <h3>Inflação</h3>
    <p>Como o euro. Há sempre moedas novas. Paga quem mantém o sistema, mas quem guarda moedas perde valor.</p>
  </div>
</div>

<p class="muted" style="margin-top:28px">Na nossa moeda, o dono emite a inflação quando quiser, até ao máximo.</p>

---v

## A taxa

- Cada pagamento paga uma percentagem **extra** para o dono da moeda.
- A loja recebe sempre o valor exato.
- Taxa alta: o dono ganha mais, mas ninguém quer usar a moeda.
- Taxa zero: toda a gente usa, mas quem mantém a moeda não ganha nada.

> O PAS paga a rede. A taxa paga quem criou a moeda. São coisas diferentes.

---

## Exercício

<p class="timer">5 minutos · em equipa</p>

- Escolham nome e símbolo.
- Decidam quantidade inicial, máximo, inflação e taxa.
- Escrevam numa frase **porquê**.

Note:

Passar pelas mesas. Perguntas boas para fazer: quem vai querer a vossa moeda? O que acontece se a taxa for 10%? Quem fica com a inflação?

---

<!-- .slide: class="hero" -->

<div class="eyebrow">parte 2 · 25 min</div>

## Lançar a <em>moeda</em>

---

## O que acontece quando carregas em lançar

<div class="flow">
  <div><b>1 · Carteira</b>A carteira junta o código do contrato com as vossas seis decisões.</div>
  <div><b>2 · Assinatura</b>A tua chave assina a transação. Ninguém a pode alterar.</div>
  <div><b>3 · Bloco</b>A rede põe a transação num bloco. Custa cerca de 0,8 PAS.</div>
  <div class="hot"><b>4 · Endereço</b>A moeda passa a viver num endereço <code>0x…</code> para sempre.</div>
</div>

---v

## O contrato

```solidity
contract Moeda is ERC20, Ownable {
    uint256 public immutable maxSupply;
    uint256 public immutable inflationBps;
    uint256 public immutable feeBps;
    address public treasury;

    function _update(address from, address to, uint256 value) internal override {
        if (from != address(0) && to != address(0) && feeBps != 0 && from != treasury) {
            super._update(from, treasury, feeFor(value));
        }
        super._update(from, to, value);
    }
}
```

Note:

ERC-20 é o padrão de moedas da Ethereum. Usamos a versão da OpenZeppelin, auditada.
A única coisa nossa é a taxa: antes de mover o valor, move a taxa para o tesouro.

---

## Faz agora

1. Toca em **Criar moeda** e preenche as decisões da equipa.
2. Toca em **Lançar** e espera pelo bloco.
3. Na página da moeda, toca em **Enviar** e dá moedas a toda a sala.

<p class="muted">Quem recebe moedas de outra equipa vê-as aparecer na carteira.</p>

---

<!-- .slide: class="hero" -->

<div class="eyebrow">parte 3 · 20 min</div>

## Pagar um <em>fino</em>

---

## O terminal

<div class="cols">
  <div>
    <ul>
      <li>Um <strong>SUNMI V3</strong>, um terminal de pagamento Android</li>
      <li>Corre uma página web, sem app instalada</li>
      <li>A loja lê o QR da vossa moeda e passa a aceitar essa moeda</li>
    </ul>
  </div>
  <div class="card">
    <h3>Uma equipa vende</h3>
    <p>Configura o terminal com a sua moeda e escreve o preço do fino.</p>
  </div>
</div>

---v

## Um pagamento, passo a passo

<div class="flow" style="--n:5">
  <div><b>terminal</b>Mostra um QR com moeda, destino e valor.</div>
  <div><b>câmara</b>Apontas o telemóvel. A carteira abre já com tudo preenchido.</div>
  <div><b>carteira</b>Mostra valor, taxa e saldo. Tocas em Pagar.</div>
  <div><b>rede</b>A transferência entra no próximo bloco, 2,4 s depois.</div>
  <div class="hot"><b>terminal</b>Vê o evento na cadeia e mostra <code>pago</code> com recibo.</div>
</div>

Note:

O terminal não precisa de servidor. Pergunta à rede, a cada 2 segundos, se chegou uma transferência com aquele valor para aquele endereço.
Cada venda tem um valor único nos últimos dígitos, para não confundir dois pagamentos iguais.

---

## Faz agora

1. Uma equipa configura o terminal com a sua moeda.
2. Escreve **2,50** e carrega em **Cobrar**.
3. Outra pessoa aponta a câmara e paga.
4. Troquem de papéis.

---

<!-- .slide: class="hero" -->

<div class="eyebrow">parte 4 · 10 min</div>

## O que <em>correu mal</em>?

---

## Perguntas para a sala

- Alguém ficou sem PAS a meio? Porque é que isso importa?
- Que moeda ninguém quis usar? Foi a taxa, a quantidade, o nome?
- Algum pagamento demorou ou não chegou?
- Quem perdeu a carteira ao fechar o browser?

Note:

Os erros são a melhor parte. Ligar cada erro a um problema real: gás, confiança, chaves perdidas, liquidez.

---

## Do teste à vida real

| Hoje | Em produção |
|---|---|
| rede de teste, PAS grátis | Polkadot Hub, DOT verdadeiro |
| contrato sem auditoria própria | auditoria antes de lançar |
| moeda sem valor | regras do MiCA na União Europeia |
| um telemóvel, uma chave | chaves partilhadas por várias pessoas |

> Uma moeda indexada ao euro é dinheiro eletrónico e precisa de licença. Um vale para cerveja, usado só no bar, quase nunca precisa.

---

<!-- .slide: class="hero" -->

# Obrigado

<p class="lead">WEB3UP, iniciativa do ACM FEUP.</p>

<div class="pills">
  <span class="primary">admin@web3up.org</span>
  <span>web3up.org</span>
</div>
