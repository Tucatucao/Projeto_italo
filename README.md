# 📊 Painel de Violência Doméstica

Este é um dashboard web desenvolvido com **Flask** para análise e visualização de dados sobre **violência doméstica** a partir de um arquivo Excel. A ferramenta oferece **gráficos interativos**, **mapas** e **ferramentas de comparação**, permitindo explorar os dados por município, região, data, natureza da ocorrência, entre outros.

Ideal para **pesquisadores**, **gestores públicos** ou qualquer pessoa interessada em compreender melhor os padrões da violência doméstica em **Pernambuco**.

---

## 🚀 Tecnologias Utilizadas

- 🔧 **Backend:** Python, Flask, Pandas, Unidecode  
- 📊 **Visualização de Dados:** Matplotlib, Folium  
- 📁 **Fontes de Dados:** Arquivos Excel (.xlsx) e GeoJSON

---

## 🛠️ Funcionalidades

- ✅ Visualização de gráficos (pizza, barras, linhas)  
- ✅ Filtros por município, região, data, sexo, idade e natureza da ocorrência  
- ✅ Geração de mapa coroplético com dados por município  
- ✅ Comparação entre dois municípios ou regiões  
- ✅ Geração dinâmica de múltiplos gráficos simultâneos  
- ✅ Exportação automática dos gráficos para a pasta `static/`

---

## 📁 Estrutura do Projeto

```
projeto/
├── app.py                      # Arquivo principal da aplicação
├── .gitignore
├── README.md
├── geojs-26-mun.json           # Arquivo GeoJSON com os municípios
├── Microdados Sobre Violencia Domestica.xlsx
├── static/
│   ├── script/                 # Arquivos JavaScript
│   ├── styles/                 # Arquivos CSS
│   ├── *.png                   # Gráficos gerados automaticamente
│   └── mapa_pernambuco.html    # Mapa interativo
├── templates/                  # Templates HTML utilizados pelo Flask
```

---

## ⚙️ Como Executar

1. Clone este repositório ou baixe os arquivos.
2. Crie e ative um ambiente virtual (recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate     # Windows
   ```
3. Instale as dependências:
   ```bash
   pip install flask pandas openpyxl matplotlib folium unidecode
   ```
4. Coloque os seguintes arquivos na raiz do projeto:
   - `Microdados Sobre Violencia Domestica.xlsx`
   - `geojs-26-mun.json`
5. Execute a aplicação:
   ```bash
   python app.py
   ```
   ou  
   ```bash
   flask run
   ```
6. Acesse no navegador:  
   [http://localhost:5000](http://localhost:5000)

---

## 🧩 Pré-requisitos

- Python 3.8 ou superior  
- pip instalado

---

## 🧠 Observações Importantes

- A aplicação cria automaticamente a pasta `static/` com os gráficos e o mapa.
- Certifique-se de que os **nomes dos municípios** no arquivo GeoJSON coincidam com os nomes no Excel.
- Para ambientes de produção, remova `debug=True` e utilize um servidor como o **Gunicorn**.

---

## ❓ Solução de Problemas

- 🔍 **Erro de dependência:** Execute `pip install -r requirements.txt` se necessário.  
- 📂 **Arquivos ausentes:** Verifique se todos os arquivos estão no diretório correto.  
- 🔄 **Porta em uso:** Altere a porta com `app.run(port=5001)` ou outra disponível.

---

## 📄 Licença

Este projeto é voltado para fins **educacionais e analíticos**, sendo distribuído livremente para estudos, pesquisas e aprimoramentos.

---

### 👨‍💻 Desenvolvido por Arthur Jose
