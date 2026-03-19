---
layout: post
type: socratic
title: "Seminário Socrático 012"
evento_so: "https://app.evento.so/e/evt_UwZFCwwmBmZYu87J"
meetup: "https://www.meetup.com/curitiba-bitdevs/events/313762932/"
---

## Avisos

- Entrem no grupo do [Whatsapp](https://chat.whatsapp.com/LTMELFt3RCb3PqIjMDqzqD) para ajudar na curadoria dos encontros!
- Entrem no Discord da [Vinteum](http://discord.gg/vinteum)
- Siga Curitiba Bitdevs no [Twitter](https://twitter.com/curitibabitdevs)
- Novos temas podem ser sugeridos nos [issues do GitHub do grupo](https://github.com/curitibabitdevs/curitibabitdevs.org/issues)
- Respeite a privacidade dos participantes.
- Os meetups nunca são gravados. Queremos todos à vontade para participar e discutir os assuntos, inclusive de forma anônima.

## Agradecimentos

- Agradecemos à [Vinteum](https://vinteum.org/) pelo apoio na organização, comidas e bebidas.  
- Agradecemos à [SEPT/UFPR](http://www.sept.ufpr.br/) e ao Prof. Mário pelo espaço cedido.

## Warmup

- Vinteum BDL Recap
- BTC++ Floripa Recap
- [Vinteum New grantee to work on P2Poolv2](https://x.com/i/status/2033949468781850935)
- [Bitcoin POW animation](https://x.com/i/status/1795165070072140201)
- [Sigbash v2](https://x.com/arbedout/status/2020885323778044259)
- [What's coming for Bitcoin Core v31](https://x.com/bitschmidty/status/2026270728698393081)
- [Mt. Gox CEO quer fazer Hard Fork no Bitcoin](https://www.coindesk.com/tech/2026/02/28/former-mt-gox-ceo-proposed-a-rewrite-of-bitcoin-s-code-to-recover-usd5-billion-in-stolen-funds-gets-quickly-shutdown)
  - [PR aberta no repositório do Bitcoin Core](https://github.com/bitcoin/bitcoin/pull/34695)
- [Dev armazena imagem de 66KB on-chain, quebra lógica do BIP-110](https://knotslies.com/)
- [O upgrade P2SH foi confiscatório?](https://xcancel.com/SuperTestnet/status/2001041017315701198)

## Bitcoin Core

- [Optech 393](https://bitcoinops.org/en/newsletters/2026/02/20/#recent-op-return-output-statistics) [Estatísticas recentes de outputs OP_RETURN](https://delvingbitcoin.org/t/recent-op-return-output-statistics/2248)
- [Optech 393](https://bitcoinops.org/en/newsletters/2026/02/20/#bitcoin-pipes-v2) [Bitcoin PIPEs v2: Covenants e ZKPs no L1 via Witness Encryption](https://delvingbitcoin.org/t/bitcoin-pipes-v2/2249)
- [Cluster Mempool mergeado no Bitcoin Core](https://github.com/bitcoin/bitcoin/pull/33629)
- [Broadcast de transações próprias via conexões Tor/I2P de curta duração](https://github.com/bitcoin/bitcoin/pull/29415)
- [rpc,net: Add private broadcast RPCs](https://github.com/bitcoin/bitcoin/pull/34329)
- [Problema de performance adversarial no scanning de silent payments (BIP-352)](https://groups.google.com/g/bitcoindev/c/tgcAQVqvzVg/m/--CkDP2xBQAJ)
- [Bitcoin core version 31 release-candidate](https://github.com/bitcoin-core/bitcoin-devwiki/wiki/31.0-Release-Notes-Draft)

## BIPs & Proposals

- [Optech 394](https://bitcoinops.org/en/newsletters/2026/02/27/#draft-bip-for-output-script-descriptor-annotations) [Draft BIP para anotações de output script descriptors com silent payments](https://github.com/craigraw/bips/blob/descriptorannotations/bip-descriptorannotations.mediawiki)

## Layer 2

- [Lightning Network ultrapassa US$ 1 bilhão em volume mensal](https://br.tradingview.com/news/cointelegraph:365de1615bc81:0/)
- [Optech 393](https://bitcoinops.org/en/newsletters/2026/02/20/#second-releases-hark-based-ark-software) [hArk — rodadas não-interativas no Ark](https://docs.second.tech/changelog/changelog/#improved-lightning-invoice-monitoring)
  - [hArk: async VTXO claims](https://x.com/2ndbtc/status/2015401100355002626)
- [Blockstream Jade integra Lightning via Atomic Swaps](https://atlas21.com/blockstream-jade-integrates-lightning-network-for-instant-payments/)
- [Extension bolt para simple taproot channels](https://github.com/lightning/bolts/pull/995)
- [RailsX: Primeira DEX nativa do Lightning](https://amboss.tech/blog/railsx-first-lightning-native-dex)

## Vulnerabilities & Bugs

- [Bug de migração de wallet presente no Bitcoin Core 30.0 e 30.1](https://xcancel.com/bitcoincoreorg/status/2008284092983369886)
- [CVE-2025-46597 — Crash remoto em sistemas 32-bit](https://bitcoincore.org/en/2025/10/24/disclose-cve-2025-46597/)
- [CVE-2025-46598 — CPU DoS via processamento de transações não confirmadas](https://bitcoincore.org/en/2025/10/24/disclose-cve-2025-46598/)
- [CVE-2025-54604 — Disco cheio via conexões falsas](https://bitcoincore.org/en/2025/10/24/disclose-cve-2025-54604/)
- [CVE-2025-54605 — Disco cheio via blocos inválidos](https://bitcoincore.org/en/2025/10/24/disclose-cve-2025-54605/)
- [LND: Infinite inbox DoS](https://morehouse.github.io/lightning/lnd-infinite-inbox-dos/)
- [LND: Replacement stalling attack](https://morehouse.github.io/lightning/lnd-replacement-stalling-attack/)
- [LND: Excessive failback exploit](https://morehouse.github.io/lightning/lnd-excessive-failback-exploit-2/)

## Research & Security

- [Blockstream demonstra assinaturas pós-quânticas no Liquid usando Simplicity](https://blog.blockstream.com/blockstream-research-demonstrates-quantum-resistant-transaction-signing-on-liquid-using-simplicity-smart-contracts/)
- [Sete cabos submarinos cortados e o Bitcoin quase não sentiu, mas provedores de nuvem são vulneráveis](https://arxiv.org/abs/2602.14372)
- [Quantum Resistance with Covenants](https://groups.google.com/g/bitcoindev/c/Sl9qQOuuAoI)
- [Nested Musig2 — paper](https://eprint.iacr.org/2026/223)
  - [Implementação no btcd](https://github.com/btcsuite/btcd/pull/2481)
- [Hash Based Signature Schema for Bitcoin](https://eprint.iacr.org/2025/2203)
- [BABE: Verificação de provas no Bitcoin 1000x mais barata](https://eprint.iacr.org/2026/065)
- [Argo MAC: Garbling with Elliptic Curve MACs](https://eprint.iacr.org/2026/049)

## Releases

- [Optech 393](https://bitcoinops.org/en/newsletters/2026/02/20/#nunchuk-adds-silent-payment-support) [Nunchuk adiciona suporte a silent payments](https://x.com/nunchuk_io/status/2021588854969414119)
- [Mastering Taproot](https://github.com/aaron-recompile/mastering-taproot)

## Miscellaneous

- [Nostr Devs lançam mesh network que elimina controle via DNS](https://nostr.com/nevent1qqsvd3nzk5p92fzp9z7p34m50039dwee0aemrvk9cl2jpng3kawsz0qzyq4m4nj48mlt7kxa2kgjz60e9sgj86mpy8tm5zf0d3gpqjhuxxkw7yqt7pf)
- [AI no open source](https://x.com/i/status/2028928215910146410)
- [Moedas não mineradas](https://x.com/i/status/2031158033032659055)
  - [Issue relacionada no mainnet-observer](https://github.com/0xB10C/mainnet-observer/issues/142)
- [Tesouro dos EUA reconhece usos legítimos de mixers ao Congresso](https://atlas21.com/usa-treasury-acknowledges-legitimate-uses-of-mixers-to-congress/)
- [Tornado Cash: Roman Storm pode pegar 40 anos enquanto governo busca novo julgamento](https://bitcoinmagazine.com/news/tornado-cashs-roman-storm-new-trial)
