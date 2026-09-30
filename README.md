# Combo Completo — PMPE

Página de venda do combo **Curso preparatório PMPE + Apostila + Caderno de questões +
Vade Mecum digital**, lançada com o edital da PMPE. Clone do `comboPMPE` (Combo Bizurado):
mesma paleta, mesmo tracking, mesmo exit popup.

**Fluxo:** clique no CTA → checkout direto, sem formulário.

## O que muda em relação ao comboPMPE

| | Valor |
|---|---|
| Checkout | `https://checkout.cppem.com.br/pay/combo-completo-pmpe` ⚠ **confirmar slug** |
| Preço | De R$ 688,00 por R$ 537,90 (-22%) · até 12x de R$ 56,12* (cartão, com acréscimo) |
| `utm_campaign` de fallback | `combo_completo_pmpe` |
| Evento `iniciar_checkout` | `produto: combo_completo_pmpe`, `valor: 537.9` |
| Chave de origem no storage | `cppem_origem_combo_completo` |
| Exit popup | `prefix: cppem_combo_completo`, `origem: exit_popup_combo_completo_pmpe` |

O botão do hero mantém o id `IPEyzyfmJhKQEYIXAlZH` da regra de clique da PixelX.
Se a regra estiver presa a outro domínio/produto, precisa ser liberada aqui.

## Assets

Reaproveitados do `comboPMPE`. O card do curso usa `everton-mota.jpg` com selo de play;
a apostila usa a capa do Resumo Bizurado (`combo-resumo.webp`). Trocar se houver
mockup próprio do curso.

## Checklist antes do disparo

- [ ] Slug do checkout confirmado em `script.js`
- [ ] Preço conferido: R$ 537,90 · 12x R$ 56,12 (topo, hero, oferta, barra fixa e rodapé)
- [ ] Checkout abriu com UTMs e `external_id`
- [ ] Regra de clique da PixelX disparando neste domínio
- [ ] Popup de saída testado com `ExitPopup.show()`
