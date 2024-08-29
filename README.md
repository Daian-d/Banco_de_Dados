# Banco_de_Dados
## Inner join
A união entte duas tabelas, consiste na junção entre chaves primária,  
<p><A identificação da chave primaria com a chave estrangeira se da pelo id de cada cvcada tabela, que identificação unica.</p>

### ⚓ 1. Tabela 'Capitão'

| CPF | Nome| Endereço | Número | Celular |
|-------------|-------------|-------------|------------|-----------|
| Chave primária| Nome do Capitão | Endereço do Capitão  | Número da residência | Número do celular|
| Tipo: bigint| Tipo: varchar| Tipo: varchar | Tipo: int | Tipo: int | Tipo: bigint|
<br>

### ⛵ 2. Tabela `escuna`
Armazena informações das escunas (barcos) utilizadas nos passeios.
| Número | Nome | capitao_CPF |
|----------|----------|----------|
| Chave primária | Nome da escuna | Chave estrangeira que referencia o CPF do capitão |
| Tipo: int| Tipo: varchar | Tipo: bigint |
<br>

### 🗺️ 3. Tabela `destino`
Armazena os destinos turísticos disponíveis.
| id | Nome |
|----------|----------|
| Chave primária com auto-incremento | Nome do destino |
| Tipo: int | Tipo: varchar |
<br>

### 🚖 4. Tabela `passeio`
Registra os passeios realizados, incluindo data, horário, escuna, e destino.
| Id | Data | Hr_saida | Hr_chegada | escuna_Numero | destino_Id |
|----------|----------|----------|----------|----------|----------|
| Chave primária com auto-incremento | Data do passeio | Hora de saída | Hora de chegada | Chave estrangeira que referencia a escuna | Chave estrangeira que referencia o destino | 
| Tipo: int | Tipo: date | Tipo: time | Tipo: time | Tipo: int | Tipo: int |
<br>
## Tabelas Relacionadad a Saúde 

### 🏥 5. Tabela Enfermeiro
- **`Enfermeiro`**: 
  
  Armazena informações dos enfermeiros responsáveis pela administração de medicamentos.<br>
  | coren | Nome |
  |--------|---------|
  | Chave primária | Nome do enfermeiro |
  | tipo: int | tipo: varchar |
  <br>
  
### 🛌 6. Tabela Paciente 
- **`Paciente`**: Registra informações dos pacientes.<br>
  
  | Num | Nome |
  |-----------|-----------|
  | Chave primária | Nome do Paciente |
  | tipo: int | Tipo: varchar |
  <br>

### ☕ 7. Tabela Remedio
- **`Remedio`**: Contém os medicamentos disponíveis.<br>

| Cod | Nome |
|----------|----------|
| Chave primária | Nome do medicamento|
| Tipo: int | Tipo: varchar | 
<br>

### 🌡️ 8. Tabela Medicamentos
- **`Medicacao`**: Registra a administração de medicamentos, relacionando pacientes, enfermeiros e remédios.<br>

| id | Data | Hora | PacienteNum | RemedioCod | Enfermeirocoren |
|----------|-----------|------------|---------------|-------------------|-------------------|
| Chave primária | Data da medicação | Hora da medicação | Chave estrangeira que referencia o paciente | Chave estrangeira que referencia  o remédio | Chave estrangeira que referencia  o enfermeiro |
| Tipo: int | Tipo: Date | Tipo: Time | Tipo: int | Tipo: int | Tipo: int |


