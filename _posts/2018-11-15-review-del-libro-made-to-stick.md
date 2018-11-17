---
layout: post
title: Review del libro Made to Stick
date: 2018-11-15 17:30 -0700
calification: 5
---
<style>
    #app{
        margin-top: 2em;
        margin-bottom:2em;
        width: 650px;
        min-height:420px;
        overflow:auto;
        padding: .7em 1.4em;
        border: 1px solid #e2e2e2;
        box-shadow: 2px 2px 20px rgba(0,0,0,.1);
        border-radius: 2px;
    }
    input {
        width: 400px;
        height: 25px;
        padding: 2px;
        margin-top: 1.5em;
        border-radius: 1px;
        border: 1px solid #e2e2e2;
    }
    button {
        width: 100px;
        height: 30px;
        padding: 2px;
        background-color: #6c5ce7;
        color: #000;
        border: none;
        border-radius: 1px;
    }
    #book_cover {
        text-align:center;
    }
</style>

<p id="book_cover">
    <a href="https://www.amazon.com/gp/product/1400064287/ref=as_li_tl?ie=UTF8&tag=tanoshii-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=1400064287&linkId=f3876d9b4cc4ec55d1b6d00a6fa6b095" target="_blank">
        <img src="https://res.cloudinary.com/yipster/image/upload/v1542415084/Made-to-stick-830x1262_jwom4v.jpg" width="40%">
    </a>
</p>

{% include stars.html %}

La meta de los autores de este libro es que comprendas por que la gente no entiende tus ideas y esta gente pueden ser potenciales clientes, o alumnos, o tu pareja, etc. La cuestión es que el libro hace un gran trabajo dándote a entender el problema y lo mejor de todo es que crea un _framework_ para que puedas pulir tus ideas y hacerlas que peguen.

Debo decir que el libro vale su peso en oro y si puedes debes ir a conseguirlo pero ya! y si no te convence permíteme que te proponga realizar una actividad aquí mismo; abajo verás un recuadro, este tiene la actividad interactiva (te lo mostraría en persona pero no te conozco y no sé donde vives). Sigue las indicaciones de esta y ya verás como las ideas que maneja el libro son realmente poderosas (está lleno de esta clase de información).

<div id="app"></div>
<script src="https://www.gstatic.com/firebasejs/5.5.8/firebase.js"></script>
<script>
    let app = document.querySelector('#app')
    app.innerHTML = `
    <h2>¿Por qué tu idea no pega?</h2>
    <p>Con suerte y después de realizar esta actividad entenderás por qué tu idea no pega, y con esto quiero decir
    que comprenderás la razón por la que tus mensajes no son captados por tus potenciales clientes, o alumnos u amigos o cualquier audiencia en cualquier ámbito.
    </p>
    <p>
    Lo único que debes hacer es escuchar el siguiente audio, el cual contiene un fragmento de canción interpretada a base de golpecitos en una mesa, 
    y adivinar que canción es; no preguntes por qué, sólo házlo, más delante obtendrás respuestas.
    </p>
    <audio controls>
    <source src="https://res.cloudinary.com/yipster/video/upload/v1542420408/tapper_gltvim.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
    </audio>
    <input type="text" name="song" id="song" placeholder="¿qué canción es?"/>
    <button name="song-button" id="verify-btn">verificar</button>
    `
</script>

<script>

    let button = document.querySelector('#verify-btn')
    let guess

    button.addEventListener('click',function(){
        guess = document.querySelector('#song').value
        if(guess === ''){
            alert('No has tratado de adivinar. \n !Vamos inténtalo!')
        }else {
            answer(guess)
        }
        
    })

    function answer(guess){
        let song = "himno de la alegría"
        if(guess.toLowerCase() === song){
             motive(true)
        }else {
            motive(false)
        }
        document.querySelector('#song').value = ''
    }

    function motive(solved){
        var title = '<h2>La respuesta</h2>'
        if(solved){
            let app = document.querySelector('#app')
            app.innerHTML = ''
            app.innerHTML = `
            ${title}
            <p>Wow, has adivinado! 😃</p>
            <p>Pero esto no es una prueba de habilidad mental, esto es una prueba para que veas que es lo que sienten tus clientes cuando escuchan tu idea (o mensaje).</p>

            <p>¿Cómo? no entendí</p>

            <p>Tu eres mi potencial cliente y el ritmo golpeteado en la mesa es mi mensaje o en otras palabras eso que has experimentado es lo que sucede cuando asumes que hay información que tu cliente sabe pero en realidad no es así y por tanto el mensaje que le envias le sonará como a tí te ha sonado el audio, a nada, a un montón de ruiditos aleatorios o a una idea que no pegará.</p>

            <p>El conocimiento que tienes se ha vuelto en tu contra y al no ser conciente de ello envías mensajes indescifrables; al yo ser la persona que realizaba los golpeteos con una canción en mente a mí me daba sentido que era el _himno de la alegría_ pero tu no sabías eso. Por tanto la canción en mi cabeza es el <b>onocimiento</b> que yo tengo y que creí tu tendrías al escuchar mis golpeteos.</p>
            <p>
            <a href="https://www.amazon.com/gp/product/1400064287/ref=as_li_tl?ie=UTF8&tag=tanoshii-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=1400064287&linkId=f3876d9b4cc4ec55d1b6d00a6fa6b095" target="_blank">Ver el libro</a>
            </p>
            `

        }else {
            app.innerHTML = ''
            app.innerHTML = `
            ${title}
            <p>Nop, en realidad es el <b>himno de la alegría</b>. ¿Huh? 😧</p>
            
            <p>Acabas de experimentar lo que tus clientes (o quien sea) sienten cuando escuchan tus ideas, desconcierto; te acabas de poner en sus zapatos.</p>
            
            <p>¿Te parece que ese ruido sonaba como el himno de la alegría? 😖 ¡En lo absoluto!</p>

            <p>Esto es lo que sucede, tú eres mi potencial cliente y el ritmo golpeteado en la mesa es mi <b>mensaje</b> o en otras palabras eso que has experimentado es lo que le sucede a un potencial cliente cuando asumes que hay información debe saber pero en realidad no es así y por tanto el mensaje que le envias le sonará como a tí te ha sonado el audio, a nada, a un montón de ruiditos aleatorios o a una idea que no pegará.</p>

            <p>El conocimiento que tienes se ha vuelto en tu contra y al no ser conciente de ello envías mensajes indescifrables.</p>
            
            <p>Al yo ser la persona que realizaba los golpeteos con una canción en mente a mí me daba sentido que era el <b>himno de la alegría</b> pero tu no sabías eso. Por tanto la canción en mi cabeza es el __conocimiento__ que yo tengo y que creí tu tendrías al escuchar mis golpeteos.</p>
            <p>
                <a href="https://www.amazon.com/gp/product/1400064287/ref=as_li_tl?ie=UTF8&tag=tanoshii-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=1400064287&linkId=f3876d9b4cc4ec55d1b6d00a6fa6b095" target="_blank">Ver el libro</a>
            </p>
            `
        }
    }

</script>