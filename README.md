# 📖 API Pokémon

A motivação inicial — e que segue sendo em um projeto futuro — é a construção de uma **Pokédex interativa**, semelhante à que construí em Power BI alguns anos atrás.  
👉 [Exemplo da Pokédex em Power BI](https://drive.google.com/file/d/1xVYkeX0bchAIEc5sfEV4crhpSwRdjsTo/view?usp=sharing)

---

## 🔗 Endpoints Utilizados

A ideia inicial era montar uma **OBT** puxando os endpoints e, em seguida, separar em tabelas no **Databricks**.  
Entretanto, como as tabelas não possuem identificadores únicos para seus atributos (apenas o identificador do Pokémon), as relações ficaram **1:1**.  

O caminho correto provavelmente seria o inverso: coletar as tabelas separadamente e depois unificá-las no Databricks.

### Endpoint principal:
GET https://pokeapi.co/api/v2/pokemon/{id|name}


- `{id}` → número do Pokémon (ex: `1` para **Bulbasaur**).  
- `{name}` → nome do Pokémon (ex: `pikachu`).  

📌 **Retorna:** todas as informações detalhadas do Pokémon:  
stats, abilities, moves, sprites, tipos, etc.

---

## 📂 Escolha dos Formatos

- **CSV** → utilizado para salvar os dados brutos da API por ser um formato simples e fácil de manipular.  
- **Parquet** → escolhido para os dados tratados, pois é mais eficiente e compatível com diversas ferramentas de análise.

---

## ⚙️ Requisitos

Certifique-se de ter os seguintes itens instalados/configurados:

- [Python](https://www.python.org/downloads)  
- [Jupyter Notebook](https://jupyter.org)  
- Conta no [Databricks Community](https://community.cloud.databricks.com/login.html)

---

✍️ **Autor:** Marcus Fonseca
