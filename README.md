# Solar Max — Landing Page

Landing page de venda e instalação de energia solar em Araras/SP e região.

Página estática única (`index.html`), sem build e sem dependências: HTML, CSS e JavaScript puro.

## Recursos

- Hero com contadores animados e ilustração SVG
- Calculadora solar — estima nº de placas, kWp, geração, economia e payback a partir do valor da conta ou do consumo em kWh
- Galeria de instalações com lightbox
- Lista de cidades atendidas
- Formulário e botões que abrem conversa no WhatsApp com mensagem pré-preenchida

## Configuração

Os parâmetros ficam no objeto `CONFIG`, no início do `<script>` em `index.html`:

```js
const CONFIG = {
  phone: '5519999999999',           // WhatsApp: 55 + DDD + número, só dígitos
  phoneDisplay: '(19) 99999-9999',  // como aparece na tela
  tarifa: 0.95,        // R$/kWh
  hsp: 5.0,            // horas de sol pleno médias
  pr: 0.78,            // fator de performance
  potenciaPlaca: 570,  // W por placa
  areaPlaca: 2.6,      // m² por placa
  custoKwp: 3800,      // R$/kWp instalado
  fatorEconomia: 0.90  // % da conta efetivamente economizada
};
```

## Pendências antes de ir para produção

- Trocar `phone` e `phoneDisplay` pelo WhatsApp real
- Substituir as fotos da galeria (hoje vêm do Unsplash) por instalações reais
- Revisar depoimentos e números da seção de estatísticas

## Rodando localmente

Basta abrir o `index.html` no navegador, ou:

```
python3 -m http.server 8000
```
