---
layout: page
title: "Contato"
description: "Alguma duvida? Eu (talvez) tenha respostas."
permalink: /contato
---
<p>Você pode entrar em contato comigo através do formulário abaixo, ou, se assim preferir, pelas redes sociais.</p>
<form name="sentMessage" id="contactForm" novalidate>
    <div class="row control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
            <label>Nome</label>
            <input type="text" class="form-control" placeholder="Nome" id="nome" required data-validation-required-message="Por favor, coloque seu nome.">
            <p class="help-block text-danger"></p>
        </div>
    </div>
    <div class="row control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
            <label>E-mail</label>
            <input type="email" class="form-control" placeholder="E-mail" id="email" required data-validation-required-message="Por favor, digite seu e-mail.">
            <p class="help-block text-danger"></p>
        </div>
    </div>
    <div class="row control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
            <label>Assunto</label>
            <input type="text" class="form-control" placeholder="Assunto" id="assunto" required data-validation-required-message="Qual o motivo do contato?">
            <p class="help-block text-danger"></p>
        </div>
    </div>
    <div class="row control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
            <label>Mensagem</label>
            <textarea rows="5" class="form-control" placeholder="Mensagem" id="mensagem" required data-validation-required-message="Por favor, deixe sua mensagem."></textarea>
            <p class="help-block text-danger"></p>
        </div>
    </div>
    <br>
    <div id="success"></div>
    <div class="row">
        <div class="form-group col-xs-12">
            <button type="submit" class="btn btn-default">Enviar</button>
        </div>
    </div>
</form>
