# 🔐 Gerador de Senhas Seguras

Uma ferramenta web para criar senhas seguras com personalização avançada e opções de cópia fácil.
<!--
![Preview do Gerador de Senhas](https://raw.githubusercontent.com/souzaseven/Site2/Desafios/icon%20eu.ico)
-->
## ✨ Funcionalidades

- **Geração Personalizada**:
  - Controle de tipos de caracteres (números, letras maiúsculas/minúsculas, símbolos)
  - Ajuste do tamanho da senha (8-64 caracteres)
  - Geração múltipla de senhas (até 10 de uma vez)

- **Recursos de Usabilidade**:
  - Cópia fácil para área de transferência
  - Limpeza rápida do conteúdo
  - Feedback visual ao copiar
  - Design responsivo

- **Segurança**:
  - Geração aleatória no cliente (não envia dados)
  - Combinações complexas de caracteres
  - Tamanho mínimo seguro padrão (16 caracteres)

## 🛠️ Tecnologias Utilizadas

- **Frontend**:
  - HTML5 semântico
  - CSS3 com Flexbox
  - JavaScript puro (ES6+)

- **Bibliotecas**:
  - Font Awesome (ícones)
  - Google Analytics (métricas)
  - Google AdSense (monetização)

## 📂 Estrutura de Arquivos
gerador-senhas/ <br>
├── index.html # Página principal <br>
├── style.css # Estilos personalizados <br>
└── script.js # Lógica do gerador<br>
<br>


## 🎨 Design e Interface

- **Tema Azul Moderno**:
  - Cores principais: Azul (#007bff) e Branco
  - Cards com sombras e bordas arredondadas
  - Ícones intuitivos

- **Tipografia**:
  - Fonte Poppins (moderna e legível)
  - Hierarquia visual clara
  - Tamanhos responsivos

- **Interações**:
  - Efeitos hover nos botões
  - Animação ao clicar
  - Transições suaves

## ⚙️ Como Funciona

### Geração de Senhas
```javascript
function generatePassword() {
    let caracteresDisponiveis = '';
    if (incluirNumeros) caracteresDisponiveis += '0123456789';
    if (incluirMinusculas) caracteresDisponiveis += 'abcdefghijklmnopqrstuvwxyz';
    // ... outros caracteres
    
    for (let i = 0; i < tamanho; i++) {
        const randomIndex = Math.floor(Math.random() * caracteresDisponiveis.length);
        senha += caracteresDisponiveis[randomIndex];
    }
}
```
### Cópia para Área de Transferência
```javascript
function copyPassword() {
    const password = document.getElementById('result');
    password.select();
    document.execCommand('copy');
    
    // Mostra feedback
    feedback.style.display = 'block';
    setTimeout(() => feedback.style.display = 'none', 2000);
}
```
