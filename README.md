# loading into page

$.get('https://raw.githubusercontent.com/e3duardo/ol/main/ol.js').then(ol=>$(document.body).append('<script>'+ol+'</script>'));
$.get('https://raw.githubusercontent.com/e3duardo/ol/main/ol.css').then(ol=>$(document.body).append('<style>'+ol+'</style>'));
