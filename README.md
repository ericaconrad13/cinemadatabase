# cinemadatabase
# S.O.S Cinema Brasileiro
{"DIRETOR":"SUSAN KATE LUND","TITULO_ORIGINAL":"CIDADE DE DEUS","CPB":"B0300002800000","PAIS_DIRETOR":"BRASIL"},
{"DIRETOR":"FERNANDO FERREIRA MEIRELLES","TITULO_ORIGINAL":"CIDADE DE DEUS","CPB":"B0300002800000","PAIS_DIRETOR":"BRASIL"},
{"DIRETOR":"JORGE ALBERTO FURTADO","TITULO_ORIGINAL":"HOMEM QUE COPIAVA, O","CPB":"B0300002700000","PAIS_DIRETOR":"BRASIL"},
{"DIRETOR":"HECTOR EDUARDO BABENCO","TITULO_ORIGINAL":"CARANDIRU","CPB":"B0300006200000","PAIS_DIRETOR":"BRASIL"},
{"DIRETOR":"KARIM AINOUZ","TITULO_ORIGINAL":"MADAME SATÃƒ","CPB":"B0300008800000","PAIS_DIRETOR":"BRASIL"},
{"DIRETOR":"GLAUBER ROCHA","TITULO_ORIGINAL":"IDADE DA TERRA","CPB":"B0400084100000","PAIS_DIRETOR":"NÃ£o Informado"},
{"DIRETOR":"GLAUBER ROCHA","TITULO_ORIGINAL":"DRAGÃƒO DA MALDADE CONTRA O SANTO GUERREIRO","CPB":"B0400084200000","PAIS_DIRETOR":"NÃ£o Informado"},
{"DIRETOR":"JOAO SERGIO BARRETO LEITE SANZ","TITULO_ORIGINAL":"EH! BOI: O BUMBA-MEU-BOI DO MARANHÃƒO","CPB":"B0500182500000","PAIS_DIRETOR":"BRASIL"},
{"DIRETOR":"RICARDO LUIS PEREIRA DE SOUZA","TITULO_ORIGINAL":"SABOTAGE - SAI DA FRENTE","CPB":"B0901064200000","PAIS_DIRETOR":"BRASIL"},

db.getCollection('filmes-brasileiros').insert({"DIRETOR":"GLAUBER ROCHA","TITULO_ORIGINAL":"TERRA EM TRANSE","CPB":"B0400079500000","PAIS_DIRETOR":"NÃ£o Informado"})

db.getCollection('filmes-brasileiros').update(

    {"DIRETOR":"GLAUBER ROCHA"},
    {$set:
     {
        "PAIS_DIRETOR": "Brasil"
     }
   }
); //editou o primeiro Glauber Rocha com "TITULO_ORIGINAL":"IDADE DA TERRA".

db.getCollection('filmes-brasileiros').update(

    {"DIRETOR":"GLAUBER ROCHA"},
    {$set:
     {
        "PAIS_DIRETOR": "Brasil"
     },
   },
 
    {
        "multi" : true, 
        
    }
    );//editou todos os "DIRETOR":"GLAUBER ROCHA"

    db.getCollection('filmes-brasileiros').find({},{"DIRETOR":1,"_id":0})//retorna o nome dos diretores.

db.getCollection('filmes-brasileiros').find().skip(1)//pulou o nome da primeira diretora Susan kate Lund e  ÚNICA mulher.
db.getCollection('filmes-brasileiros').find({})// para aparece todos de novo
db.getCollection('filmes-brasileiros').find().limit(1)//retorna a primeira diretora.
