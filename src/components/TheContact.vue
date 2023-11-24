<template>
    <div class="caixa-contato">
        <div class="info-contato">
            <h4>Contato</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. <br>Ducimus at hic architecto libero deleniti!<br> Ea
                quos dolorem ad, obcaecati aspernatur <br> placeat libero facere fugiat <br>repellat ut vero modi accusantium in.
                <br>Lorem ipsum dolor sit amet consectetur adipisicing elit. <br>Nemo voluptatum doloribus accusamus soluta, <br> perspiciatis tempora tenetur suscipit distinctio <br> harum maxime neque commodi repudiandae ullam, in animi <br> fugit cumque illum facilis.
            </p>
        </div>
        <div class="sugestoes">
            <h3>Sugestões?</h3>
            <form action="#" method="get">
                <input type="text" id="email" name="email" placeholder="Email" v-model="email">
                <span></span>
                <input type="text" id="escreverSugestao" name="escreverSugestao" placeholder="Escreva aqui..." v-model="escreverSugestao">
                <span></span>
                <input id="button" type="submit" value="Enviar">
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: "TheContact",
    components: {}

}
</script>

<style>
.caixa-contato {
    color: #FFF;
    display: flex;
    background-color: #062B00;
    padding: 20px 20px 20px 20px;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 250px;
    margin-right: 20px;
    overflow-x: hidden;
}
.caixa-contato span{
    display: block;
}
.caixa-contato .info-contato{
    text-align: center;
}

.caixa-contato .info-contato h4{
    font-size: 24px;
    font-weight: bold;
}

.caixa-contato .sugestoes{
    position: relative;
    right: 60px;
    padding: 20px 4px 5px 4px;
    margin-bottom: 12px;
    border-left: 3px #fff solid;
    padding-left: 40px;
}
.caixa-contato .sugestoes h3{
    position: relative;
    left: 40px;
    font-size: 24px;
}
.caixa-contato .sugestoes input{
    margin-bottom:20px;
}

.sugestoes #escreverSugestao{
    height: 38px;
}
.sugestoes #email,#escreverSugestao{
    width: 200px;
}

.sugestoes #button{
    position: relative;
    left: 112px;
    padding: 4px 6px 4px 6px;
    width: 95px;
    background-color: #ABE497;
    color: #000;
    font-weight: bolder;
}

</style>