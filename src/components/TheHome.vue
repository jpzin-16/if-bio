<template>
    <div>
        <div id="caixa-titulo">
           <strong><h3>"A biologia é a ciência. A evolução é o conceito que faz a biologia ser única."</h3></strong>
        </div>
        <div class="caixa-carrossel">
            <div class="carrossel-imagens">
                <TheSlider />
                <div class="desc-int">
                    <h2 id="integrantes">integrantes</h2>
                    <p id="descricao">Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda veniam <br> aspernatur
                        quidem excepturi at, cumque dicta possimus nemo dolore <br>officiis, maiores est corrupti dolorum
                        deleniti, <br>dolores nobis eaque! Ipsum, corporis.</p>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>
import TheSlider from './TheSlider.vue';

export default {
    name: 'TheHome',
    components: { TheSlider },
    data() {
        return {}
    },
}
</script>
  
<style>
#caixa-titulo {
    border: 0;
    padding: 14px;
    background-color: #C1FBD1;
    width: 100%;
    height: 150px;
    overflow-x: hidden;
}

#caixa-titulo h3 {
    text-align: center;
    color: #000;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 23.9px;
    justify-content: center;
    position: relative;
    top: 45px;
}

.carrossel-imagens {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 450px;
    padding: 20px 10px 20px 10px;
    background-color: #062B00;
    flex-direction: row;
}

.carrossel-imagens .desc-int {
    padding: 10px 10px 10px 10px;
    margin: 0
}

.carrossel-imagens #img-pj {
    width: 650px;
    height: 450px;
    position: relative;
}

.carrossel-imagens .desc-int #integrantes {
    color: #FFF;
    font-size: 27px;
    text-align: center;
    text-transform: uppercase;
}

.carrossel-imagens .desc-int #descricao {
    color: #FFF;
    font-size: 20px;
    text-indent: 5%;
    text-align: center;
}
</style>
  