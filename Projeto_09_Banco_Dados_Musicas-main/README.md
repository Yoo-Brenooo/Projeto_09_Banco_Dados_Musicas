# 🎵 Projeto de Banco de Dados - Análise Musical

## 📋 Descrição do Projeto
Este projeto consiste na criação e manipulação de um banco de dados SQLite contendo informações sobre músicas, artistas, álbuns, gêneros e streaming. Os alunos foram contratados para implementar e analisar os dados musicais.

## 🗄️ Estrutura do Banco de Dados

### Tabela `musicas`
| Coluna | Tipo | Descrição |
|--------|------|-----------|
| id | INTEGER | Chave primária (auto increment) |
| titulo | TEXT | Título da música |
| artista | TEXT | Nome do artista/banda |
| album | TEXT | Nome do álbum |
| genero | TEXT | Gênero musical |
| duracao_segundos | INTEGER | Duração em segundos |
| ano_lancamento | INTEGER | Ano de lançamento |
| streaming_count | INTEGER | Contagem de streams |

## 🎯 Objetivos do Projeto

Os alunos devem criar queries SQL para responder às seguintes perguntas de negócio:

### 📊 Análises Solicitadas

1. **Álbuns do Michael Jackson na lista e anos de lançamento**
2. **Músicas de Rock da playlist**
3. **Músicas lançadas nos anos 90**
4. **Músicas lançadas a partir dos anos 2000**
5. **Adicionar música favorita do aluno**
6. **Adicionar música de Funk que o professor odeia**
7. **Remover música adicionada anteriormente**
8. **Quantidade de músicas da banda AC/DC**
9. **Quantidade de músicas de POP na playlist**
10. **Ordenar músicas da mais velha para a mais nova**

## 💾 Scripts SQL

### Criação da Tabela
```sql
CREATE TABLE musicas (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    titulo TEXT NOT NULL,
    artista TEXT,
    album TEXT,
    genero TEXT,
    duracao_segundos INTEGER,
    ano_lancamento INTEGER,
    streaming_count INTEGER
);
```

### Inserção de Dados
```sql
-- Exemplo de inserção (100+ músicas incluídas no projeto)
INSERT INTO musicas (titulo, artista, album, genero, duracao_segundos, ano_lancamento, streaming_count) VALUES
('Bohemian Rhapsody', 'Queen', 'A Night at the Opera', 'Rock', 354, 1975, 2500000000),
('Blinding Lights', 'The Weeknd', 'After Hours', 'Pop', 200, 2019, 3500000000),
-- ... (demais músicas)
```



## 📊 Queries Adicionais para Análise

### Artistas com mais músicas na playlist
```sql
SELECT artista, COUNT(*) as total_musicas 
FROM musicas 
GROUP BY artista 
ORDER BY total_musicas DESC 
LIMIT 10;
```

### Músicas mais longas
```sql
SELECT titulo, artista, duracao_segundos 
FROM musicas 
ORDER BY duracao_segundos DESC 
LIMIT 10;
```

### Músicas mais populares (mais streams)
```sql
SELECT titulo, artista, streaming_count 
FROM musicas 
ORDER BY streaming_count DESC 
LIMIT 10;
```

### Distribuição por gênero musical
```sql
SELECT genero, COUNT(*) as total_musicas 
FROM musicas 
GROUP BY genero 
ORDER BY total_musicas DESC;
```

## 🛠️ Tecnologias Utilizadas

- **SQLite** - Banco de dados
- **DB Browser for SQLite** - Interface gráfica
- **SQL** - Linguagem de consulta

## 📈 Habilidades Desenvolvidas

- ✅ Criação e manipulação de tabelas SQL
- ✅ Inserção de dados em massa
- ✅ Consultas SELECT com filtros complexos
- ✅ Operadores BETWEEN, LIKE, IN
- ✅ Funções agregadas (COUNT)
- ✅ Operações DELETE e INSERT
- ✅ Ordenação de resultados (ORDER BY)
- ✅ Análise de dados musicais
- ✅ Trabalho com datas e intervalos temporais

## 👥 Equipe
Projeto desenvolvido pelos alunos como parte do exercício prático de banco de dados.

## 📄 Licença
Este projeto é para fins educacionais.

---

*Projeto desenvolvido para praticar habilidades SQL e análise de dados no contexto musical.* 🎵✨

## 💡 Dicas para os Alunos

1. **Use aliases** para tornar os resultados mais legíveis
2. **Teste cada query** individualmente antes de entregar
3. **Verifique os dados** inseridos após cada operação
4. **Use WHERE clauses** específicas para evitar deletar dados errados
5. **Documente suas queries** com comentários

**Bom trabalho!** 🎶
