Luiz Fernando 
/
Formulário

Código
Solicitações de pull
38
Ações
Projetos
Segurança
Percepções
Comprometer-se
página de formulário com HTML e CSS
 mestre
@uiz_harrow
Luifernando comprometido em 06 de agosto de 2024 
0 pais
cometer fd9fc4c
 
Exibindo 2 arquivos alterados com 234 adições e 0 exclusões .
Filtrar arquivos alterados
 122 alterações: 122 adições e 0 exclusões122 
formulario.css
Número da linha do arquivo original	Número da linha de diferença	Mudança de linha diferencial
@@ -0,0 +1,122 @@
/* Todos os elementos da página */
* {
    margem :  0 ;
    preenchimento :  0 ;
}

/* Elementos com o ID "título" */
# título {
    família de fontes : sans-serif;
    cor :  # 380B61 ;
    margem esquerda :  7 % ;
}

/* Elementos com o ID "subtítulo" */
# legenda {
    família de fontes : sans-serif;
    cor :  # 380B61 ;
    margem esquerda :  10 % ;
}

# verificar {
    exibição : bloco embutido;
}

/* Elementos da tag <fieldset>*/
conjunto de campos {
    borda :  0 ;
}

/* Elemento de tag <body> */
corpo {
    cor de fundo :  # F0F8FF ;
    família de fontes : sans-serif;
    tamanho da fonte :  1 em ;
    cor :  # 59429d ;
    margem esquerda :  36 % ;
    margem superior :  2 % ;
    justificar-conteúdo : centro;
}

/* Elementos de tags <body>, <input>, <Select>, <textarea> e <button> */
entrada ,  selecionar ,  textarea ,  botão {
    família de fontes : sans-serif;
    tamanho da fonte :  1 em ;
    cor :  # 59429d ;
    raio da borda :  5 px ;
}

/* Elementos de classe "grupo" nos estados das pseudoclasses "before" e "after" */
. grupo : antes , . grupo : depois {
    exibição : tabela;
}

/* Elementos de classe "grupo" no estado da pseudoclasse "after" */
. grupo : depois {
    limpar ambos ;
}

/* Elementos de classe "campo" */
. campo {
    margem-inferior :  1 em ;
}

/* Elementos de classe "campo" da tag <label> */
. rótulo do campo  {
    margem inferior :  0,2 em ;
    cor :  # 59429d ;
    exibir : bloco;
}

/* Elementos de classe "campo" ou "grupo" da tag <fieldset> */
fieldset . grupo . campo {
    flutuar :   esquerda;
    margem-direita :  1 em ;
}

/* Elementos de classe "campo" das tags <input> com atributo text e email, da tag <select> e da tag <textarea>*/
. campo  input [ tipo = "texto" ] , . campo  input [ tipo = "email" ] , . campo  select , . campo  textarea {
    preenchimento :  0,2 em ;
    borda :  1 px sólido # 59429d ;
    caixa-sombra :  2 px  2 px  2 px  rgba ( 0 , 0 , 0 , 0.2 );
    exibir : bloco;
}

/* Elementos de classe "campo" da tag <select> e <option>*/
. campo  selecione  a opção {
    preenchimento-direito :  1 em ;
}

/* Elemento de classe "campo" com tag <input>, <select> e <textarea> tocas com estado da pseudoclasse "focus"*/
. campo  input : foco , . campo  select : foco , . campo  textarea : foco {
    fundo :  # E0E0F8 ;
}
