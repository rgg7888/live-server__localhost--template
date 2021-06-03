# live-server__localhost--template
<pre>
<?php require_once './Herramientas.php';
copy('./main.css', '/var/www/html/main.css');
copy('./ajax.txt', '/var/www/html/ajax.txt');
#############################Live Server + Localhost##################
$pagina = documento().
contenedor([
    cabeza([
        estilo(),
        titulo(),
        favicon()
    ]),
    cuerpo([
        generico('n','a',['href'=>'http://localhost:3000'],'Home'),
        generico('n','div',['id'=>'demo'],[
            generico('n','h2',['class'=>'titulo'],'AJAX'),
            generico('n','button',[
                'type' => 'button',
                'onclick' => 'loadDoc()'
            ],'Change Content')
        ])
    ])
]).js();
crearArchivoHtml('../../../../var/www/html/index.html',$pagina);
header('Location: http://localhost');
</pre>
