# 🔐 Criptografia Assimétrica Inspirada em RSA

Implementação em Python de um sistema de criptografia assimétrica inspirado no RSA, com geração dinâmica de chaves baseada em propriedades matemáticas e uso de dígitos de π.

# 📌 Sobre o Projeto

Este projeto implementa um modelo de criptografia assimétrica inspirado no algoritmo RSA, com algumas adaptações criativas na geração de números utilizados na chave. <br>
<br>
O sistema permite: <br>

Criptografar mensagens <br>
Descriptografar mensagens <br>
Gerar automaticamente chaves públicas e privadas

# ⚙️ Como Funciona

O algoritmo segue a base do RSA, com diferenciais na geração dos números: <br>

🔢 1. Geração dos Blocos <br>
 <br>
Números são gerados a partir de dígitos de π (pi) com alta precisão (mpmath) <br>
São criados blocos pseudoaleatórios <br>
Os valores passam por verificações (não divisíveis por 2, 3 ou 5) <br>
<br>
🔑 2. Geração das Chaves <br>
<br>
Dois blocos a e b são gerados <br>
Calcula-se: <br>
n = a × b <br>
φ(n) (totiente) via fatoração <br>
Escolha do expoente público: <br>
e coprimo com φ(n) <br>
Cálculo da chave privada: <br>
d = inverso modular de e mod φ(n) <br>
<br>
🔐 3. Criptografia <br>
<br>
Cada caractere da mensagem é convertido para número (ASCII) e criptografado: <br>
C = (M^e) mod n <br>
<br>
🔓 4. Descriptografia <br>
<br>
A mensagem é recuperada com: <br>
M = (C^d) mod n

# 🖥️ Interface do Programa

O sistema funciona via terminal com menu interativo: <br>
<br>
1. Criptografar <br>
2. Descriptografar <br>
3. Sair

# 🚀 Funcionalidades

✔ Geração automática de chaves <br>
✔ Criptografia de mensagens texto <br>
✔ Descriptografia com validação <br>
✔ Uso de matemática aplicada (totiente, MDC, inverso modular) <br>
✔ Sistema baseado em RSA com adaptação criativa

# 🛠️ Tecnologias Utilizadas
Python <br>
Biblioteca mpmath (alta precisão) <br>
math (operações matemáticas) <br>
random (geração pseudoaleatória)

# ▶️ Como Executar
Instale as dependências: <br>
pip install mpmath <br>
Execute o script: <br>
python main.py

# 💡 Exemplo de Uso
Mensagem: "Lucas" <br>
<br>
Saída criptografada: <br>
[374426668, 729392, 39448098, ...] <br>
<br>
Chaves geradas: <br>
E = 7 <br>
N = 377736821 <br>
D = 151195063

# ⚠️ Observações Importantes
Este projeto é educacional e não deve ser usado em sistemas reais de segurança <br>
O uso de eval() pode representar riscos — ideal substituir em versões futuras <br>
A geração de números não segue padrões criptográficos seguros de produção

# 📈 Visão de Melhoria
 Substituir eval() por método seguro <br>
 Interface gráfica (GUI) <br>
 Melhorar geração de números primos <br>
 Implementar padding seguro <br>
 Otimização de performance
 
# 🎯 Objetivos do Projeto
Praticar conceitos de criptografia <br>
Entender o funcionamento do RSA <br>
Aplicar matemática na programação <br>
Desenvolver lógica avançada

# 🔥 Diferenciais
Uso criativo de π para geração de números <br>
Implementação manual de conceitos matemáticos <br>
Sistema completo (criptografia + descriptografia) <br>
Projeto forte para portfólio na área de segurança

# 👨‍💻 Autor

Lucas Ramos <br>
🎓 Estudante de Ciência da Computação
