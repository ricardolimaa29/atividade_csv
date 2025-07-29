# 🧪 Exercício: Análise Simples de Alunos com CSV

## 📝 Enunciado

Você recebeu um arquivo chamado `alunos.csv` com os seguintes dados:

```csv
nome,idade,nota
Alice,17,8.5
Bruno,18,7.0
Carla,17,9.2
Diego,19,6.8
```

Crie um script em Python que:

1. Leia o conteúdo do arquivo CSV.

2. Mostre o nome de todos os alunos com nota maior ou igual a 7.

3. Exiba a média das notas da turma.

import csv 

with open("dados.csv", newline="",encoding="utf-8") as arquivo:
    leitor = csv.DictReader(arquivo)
    for linha in leitor:
        nome = linha["nome"]
        nota = float(linha["nota"])
        if nota > 7:
            print(f"{nome} esta aprovado com sucesso ! 😁")
        media = sum(float(linha["nota"]) for linha in leitor) / len(linha["nota"])
        print(f"a media é: {media:.2f} ")
    

