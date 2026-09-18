---
layout: post
published: true
type: socratic
title: "Seminário Socrático 018"
evento_so: "https://app.evento.so/e/evt_66gibXLHh9Vqdqjk"
---

## Avisos

- Entrem no grupo do [Whatsapp](https://chat.whatsapp.com/LTMELFt3RCb3PqIjMDqzqD) para ajudar na curadoria dos encontros!
- Entrem no Discord da [Vinteum](http://discord.gg/vinteum)
- Siga Curitiba Bitdevs no [Twitter](https://twitter.com/curitibabitdevs)
- Sugestões e referências completas estão na [issue de tópicos deste encontro](https://github.com/curitibabitdevs/curitibabitdevs.org/issues/65).
- Respeite a privacidade dos participantes.
- Os meetups nunca são gravados. Queremos todos à vontade para participar e discutir os assuntos, inclusive de forma anônima.

## Agradecimentos

- Agradecemos à [Vinteum](https://vinteum.org/) pelo apoio na organização, comidas e bebidas.  
- Agradecemos à [SEPT/UFPR](http://www.sept.ufpr.br/) e ao Prof. Mário pelo espaço cedido.

## Warmup

- [BitDevs pelo Brasil](https://bitdevs.com.br/) ([integração no site](https://github.com/curitibabitdevs/curitibabitdevs.org/pull/66))
- [Curitiba BitDevs no site do Miguel Medeiros](https://miguelmedeiros.dev/) ([anúncio](https://x.com/_miguelmedeiros/status/2097872142507413969))

## Discussão principal

Vamos priorizar os quatro temas abaixo. As referências de cada tema ficam agrupadas para uma única discussão. Depois vêm as atualizações rápidas e, ao final, os tópicos de menor prioridade, para consulta ou discussão se houver tempo.

### Core Lightning: vulnerabilidades e divulgação das correções

- [Anúncio da atualização de segurança](https://x.com/Core_LN/status/2092755509510283423)
- [Release de segurança 26.06.7 e publicação adiada do código-fonte](https://blog.blockstream.com/core-lightning-26-06-7/)
- [Código e notas da release v26.06.7](https://github.com/ElementsProject/lightning/releases/tag/v26.06.7)
- [Divulgação do DoS por flood de pings, corrigido na v25.09](https://delvingbitcoin.org/t/disclosure-crashing-cln-with-a-flood-of-pings/2846)

### Liquid: exploração, recuperação de fundos e retomada da rede

- [Relato do incidente pela Liquid](https://x.com/Liquid_BTC/status/2096696272447218108)
- [Atualização sobre a retomada dos blocos e a situação do peg](https://x.com/Liquid_BTC/status/2098025275921490281)
- [Devolução parcial dos fundos e saldo ainda pendente](https://cointelegraph.com/news/liquid-white-hats-return-270m-bitcoin-network-restart)
- [Relatório independente sobre o incidente: kimi_report_liquid_hack](https://gist.github.com/1440000bytes/211ac92dd4433bb1a2e674bf0ff7db2e)

### LND: confirmações no fechamento de canais e risco de reorganização

- [Divulgação da falha no acompanhamento de canais fechados](https://delvingbitcoin.org/t/disclosure-lnd-doesnt-wait-for-enough-confirmations-when-closing-channels/2800)

### Silent Payments: uso no Electrum e privacidade no longo prazo

- [Plugin de envio de Silent Payments para Electrum](https://delvingbitcoin.org/t/silent-payments-sender-bip352-plugin-for-electrum/2743)
- [Risco de perda futura de privacidade: harvest-now-decrypt-later](https://conduition.io/cryptography/hndl-silent-payments/)

## Atualizações rápidas

- [Bitcoin Core: redução do espaço em disco do txindex](https://github.com/bitcoin/bitcoin/pull/35531)
- [BOLT 12: payer proofs incorporados à especificação](https://github.com/lightning/bolts/pull/1346)
- [HWI: plano de manutenção mínima e BHWI como possível sucessor](https://github.com/bitcoin-core/HWI/issues/850) ([reportagem](https://livecoins.com.br/bitcoin-core-se-prepara-para-encerrar-desenvolvimento-de-ferramenta-que-oferece-suporte-para-carteiras-de-hardware/))

## Tópicos de menor prioridade

Referências complementares para leitura e comentários breves, caso sobre tempo no encontro.

- [RoninDojo v3.0.0](https://x.com/RoninDojoNode/status/2089699332786200840)
- [Prem AI anuncia CyberScan para auditorias de segurança](https://decrypt.co/376056/prem-ai-launches-cyberscan-for-continuous-ai-security-audits-of-bitcoin-infrastructure)
- [Iceberg: novo paper sobre custódia threshold na Lightning com assinaturas aninhadas](https://eprint.iacr.org/2026/1757)
- [StarkWare demonstra transação resistente a ataques quânticos na mainnet](https://cointelegraph.com/news/starkware-quantum-resistant-bitcoin-transaction-mainnet)
- [Chainalysis estima volume de atividade tributável](https://atlas21.com/chainalysis-estimates-457-billion-in-taxable-activity/)
- [Comunicado da OCEAN e de Luke Dashjr sobre sua saída](https://www.prnewswire.com/news-releases/joint-statement-of-ocean-and-luke-dashjr-302864347.html)
- [Desdobramento do caso Coldcard: movimentação dos fundos pela THORChain](https://atlas21.com/galaxy-says-coldcard-hacker-swapped-stolen-bitcoin-on-thorchain/)
- [Fabricantes de carteiras pedem divulgação responsável de vulnerabilidades](https://x.com/P3b7_/status/2096954475952910513)
- [CoinCorner anuncia cofre multisig com seguro](https://x.com/CoinCorner/status/2097282633407344676)
- [Amboss e Aureo conectam a Lightning ao sistema bancário mexicano](https://www.globenewswire.com/news-release/2026/09/09/3358873/0/en/amboss-and-aureo-connect-the-lightning-network-to-mexico-s-banking-system.html)
- [Proposta Segregated Data: região de bloco podável para dados arbitrários](https://delvingbitcoin.org/t/bip-draft-segregated-data-a-prunable-script-isolated-block-region-for-data-carriage/2641)
- [Proposta de Conditional Message Transfer Contract (CMTC) contra channel jamming](https://delvingbitcoin.org/t/conditional-message-transfer-contract-to-solve-jamming/2772)
- [Relato de suposto backdoor na Wasabi Wallet](https://x.com/caueconomy/status/2088345502223863957)
- [Peter Todd retoma a proposta de emissão de cauda](https://livecoins.com.br/emissao-de-cauda-pode-ser-a-proxima-grande-polemica-do-bitcoin-entenda-a-proposta/)
