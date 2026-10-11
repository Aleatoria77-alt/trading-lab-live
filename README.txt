# Trading Lab Live

Painel estático responsivo que consulta candles reais da API pública da Binance Spot. Não precisa de chave para esse teste.

## O que está implementado
- Candles reais por REST API pública da Binance.
- Timeframes 1m, 3m, 5m, 15m, 1h, 4h e 1d.
- Seleção de criptoativos Spot listados no painel.
- EMA 9/21, Bollinger, RSI(14), MACD e níveis simples de suporte/resistência calculados a partir dos candles recebidos.
- Estimativa direcional técnica (ALTA/BAIXA/NEUTRO) baseada em regras explícitas; não é probabilidade estatística validada.
- Estado de erro sem inventar cotações ou sinais quando a API falha.

## Limitações
- Somente cripto Spot da Binance. Não inclui Forex, ações, índices, commodities ou preços OTC da IQ Option.
- A atualização é por consulta periódica REST; não é WebSocket.
- Não executa ordens nem se conecta à conta da corretora.
- O acesso à API depende de internet, disponibilidade da Binance, limites da API e suporte do navegador.
- Indicadores e estimativas são informativos, não garantem direção futura.

## Publicar gratuitamente com GitHub Pages
1. Entre em https://github.com e crie um repositório público, por exemplo `trading-lab-live`.
2. Envie `index.html` para a raiz do repositório. Renomeie `trading_lab_live.html` para `index.html`.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, selecione a branch `main` e a pasta `/ (root)`, e salve.
5. Aguarde a publicação. O GitHub mostrará a URL pública na seção Pages.

## Teste local
Abra `trading_lab_live.html` em um navegador moderno com internet. Se a API ou o navegador bloquear a solicitação, o painel mostrará estado de erro e não apresentará o sinal como válido.

## Fonte
Endpoint de candles usado: `https://api.binance.com/api/v3/klines`
