const express = require('express');
const app = express();
const post = 3000;

app.use(express.json());

let nomes =[];

app.post('/adicionar-nome', (req, res)=> {
const nome = req.body.nome;
if (nome){
    nomes.push(nome);
    res.status(201).send(`Nome ${nome} Adiciondo com sucesso!`)
} else {
    res.s;tatus(400).send('Nome é obrigatório.')
}});

app.listen(post, () =>{
console.log(`Servidor rodando em <http://localhost>:${post}`);
});
