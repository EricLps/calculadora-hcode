# 📟 Calculadora Hcode

Bem-vindo à documentação oficial da **Calculadora Hcode**, uma calculadora web moderna e funcional, desenvolvida como parte do curso de JavaScript da Hcode Treinamentos.

Este projeto serve como um ótimo estudo de manipulação do DOM, tratamento de eventos, uso de classes em JavaScript e integração com recursos como áudio, clipboard e exibição de data/hora.

---

## 🚀 Funcionalidades Principais

- ✅ Operações básicas: soma, subtração, multiplicação, divisão e porcentagem.
- ⌨️ Entrada via teclado e mouse: digite ou clique nos botões.
- 📋 Suporte a clipboard: copie (Ctrl+C) e cole (Ctrl+V) valores diretamente.
- 🔊 Áudio: duplo clique no botão `AC` ativa/desativa o som de clique.
- 🕒 Exibição de data e hora sempre atualizadas no topo.
- ⚠️ Tratamento de erros: entradas inválidas exibem `"Error"` no display.
- 📱 Interface responsiva: utilizável em desktop e dispositivos móveis.

---

## 🏗️ Estrutura da Classe

### 🔧 `constructor()`

Inicializa:

- Elementos do DOM (display, data, hora)
- Áudio e suas configurações
- Array de operações
- Eventos principais de interação

```js
const calc = new CalcController(); // A calculadora já estará pronta para uso
````

### 🖱️ Métodos de Inicialização
initialize()
- Atualiza data e hora a cada segundo.

- Exibe o último número no display.

- Ativa recurso de colar do clipboard.

- Permite ativar/desativar áudio com duplo clique no botão AC.

initButtonsEvents()
- Adiciona eventos de clique, arraste e mouse aos botões SVG.

initKeyboard()
- Permite controlar a calculadora totalmente pelo teclado.

- Suporta Ctrl+C (copiar) e Ctrl+V (colar).

###  🧮 Métodos de Operações
addOperation(value)
- Adiciona números ou operadores à operação atual.

- Atualiza o display dinamicamente.

pushOperation(value)
- Adiciona um valor ao array de operações.

- Realiza cálculos automaticamente quando há mais de 3 itens.

calc()
- Executa o cálculo da expressão atual.

- Suporta operações encadeadas e uso de % como porcentagem.

getResult()
- Utiliza eval() para calcular o resultado.

- Em caso de erro, exibe "Error" no display.

### 📋 Manipulação de Clipboard
- copyToClipboard()
- Copia o valor atual do display para a área de transferência.

- Usa navigator.clipboard com fallback para navegadores antigos.

- pasteFromClipboard()
- Permite colar diretamente valores no display.

### 🔊 Controle de Áudio
toggleAudio()
- Liga/desliga o som de clique da calculadora.

playAudio()
- Toca o som ao clicar, se ativado.

### 🕒 Exibição de Data e Hora
setDisplayDateTime()
- Atualiza automaticamente os elementos de data e hora.

### 🛠️ Métodos Auxiliares
- clearAll(): Limpa toda a operação.

- clearEntry(): Remove o último item digitado.

- setError(): Exibe "Error" no display.

- addDot(): Adiciona ponto decimal.

- getLastOperation(), setLastOperation(value), getLastItem(isOperator): Manipulam o array de operações internamente.

###  📟 Getters/Setters
- displayCalc: Valor exibido no display principal.

- displayDate: Data exibida.

- displayTime: Hora exibida.

- currentDate: Data/hora atual do sistema.

###  📁 Estrutura de Arquivos

````
/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── CalcController.js
├── media/
│   └── click.mp3
└── README.md
````

###  ⚠️ Observações Importantes
O áudio click.mp3 deve estar na pasta /media, no mesmo nível do HTML principal.

Utilize sempre barra / no caminho do áudio (ex: 'media/click.mp3').

O display aceita até 10 caracteres. Acima disso, será exibido "Error".

###  💡 Dicas de Uso

| Ação                   | Atalho                              |
| ---------------------- | ----------------------------------- |
| Ativar/Desativar áudio | Duplo clique no botão `AC`          |
| Copiar valor           | `Ctrl + C` com o display focado     |
| Colar valor            | `Ctrl + V` ou botão direito > Colar |

###  👨‍💻 Contribuindo
Contribuições são bem-vindas! Se quiser sugerir melhorias, corrigir bugs ou adicionar novas funcionalidades, sinta-se à vontade para abrir uma issue ou pull request.

###  📚 Créditos
Este projeto foi desenvolvido como parte do curso de JavaScript da Hcode Treinamentos.
