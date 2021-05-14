# Fix TNT Brasil Radar

O radar/mapa da localização do TNT Brasil não está funcionando, e se for um erro do cliente, conforme estou esperando, vou tentar corrigir aqui do meu lado

Link do radar: https://radar.tntbrasil.com.br/radar/public/localizacaoSimplificada

Como a página usa jQuery, é só rodar isto no console navegador antes de abrir a página do radar
```
$.get('https://raw.githubusercontent.com/e3duardo/ol/main/ol.js').then(ol=>$(document.body).append('<script>'+ol+'</script>'));
$.get('https://raw.githubusercontent.com/e3duardo/ol/main/ol.css').then(ol=>$(document.body).append('<style>'+ol+'</style>'));
```

Detectei que a página está tentando carregar dois arquivos com http, sendo que ela é https, porém só carregar estes aquivos com https ainda não resolveu.

Mapa antes da aplicação do patch
![Mapa com problema](https://github.com/e3duardo/fix-tnt-brasil-radar/blob/main/Captura%20de%20tela%20de%202021-05-14%2010-48-38.png?raw=true)

Mapa depois da aplicação do patch
![Mapa após o path](https://github.com/e3duardo/fix-tnt-brasil-radar/blob/main/Captura%20de%20tela%20de%202021-05-14%2010-48-00.png?raw=true)

Como notado, o mapa volta a funcionar, mas ainda não exibe nenhuma informação, isso pode ainda ser algo do client, ou pode ser algo de backend. Vou analizar mais detalhadamente e retorno aqui com a solução (se for algo do client) ou não.
