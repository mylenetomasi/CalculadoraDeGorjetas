<script>
export default {
    data () {
        return {
            qualidades: [
                {porcentagem: "5%", servico: "serviço péssimo"},
                {porcentagem: "10%", servico: "serviço ruim"},
                {porcentagem: "15%", servico: "serviço OK"},
                {porcentagem: "20%", servico: "serviço bom"},
                {porcentagem: "25%", servico: "serviço mais que bom"},
                {porcentagem: "30%", servico: "serviço excepcional"},
            ]
        }
    }
};
</script>
<template>
    <main>
        <div class="calc">
            <h1>Calculadora de <strong>Gorjetas</strong></h1>
            <div class="valores-forms">
                <label for="input-valor">Qual o valor da conta?</label>
                <input id="input-valor" type="number">
            </div>
            <div class="valores-forms">
                <label for="select-servico">Como foi o serviço?</label>
                <select name="select-qualidade" id="select-servico">
                    <option v-for="porcentagem of qualidades" :key="porcentagem.porcentagem" for="select-servico" value="porcentagem.porcentagem">{{ qualidades.servico }}</option>
                </select>
            </div>
            <div class="valores-forms">
                <label for="input-pessoas">Quantas pessoas estão pagando a conta?</label>
                <input id="input-pessoas" type="number">
            </div>        
        </div>
        <div class="resultado">
            <h2>Valor da conta:</h2>
            <span>R$ 0.00 por pessoa</span>
        </div>
    </main>
</template>