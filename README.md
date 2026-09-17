# Gerador e Validador Quartz Cron

Uma ferramenta completa, moderna e totalmente independente para gerar, validar, traduzir e prever execuções de expressões **Quartz Cron** (6 ou 7 campos).

Desenvolvida em um único arquivo **XHTML estrito** (`index.xhtml`), pronta para uso sem necessidade de conexão com a internet, servidores locais, Node.js ou instalação de qualquer dependência.

---

## 🚀 Como Usar

1. Basta abrir o arquivo `index.xhtml` em qualquer navegador web moderno (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari, Opera, etc.):
   - **Duplo-clique** no arquivo `index.xhtml`; ou
   - Clique com o botão direito e selecione **"Abrir com"** &rarr; seu navegador de preferência.
2. Você pode usá-lo em qualquer computador, mesmo totalmente sem internet.

---

## ✨ Recursos

- **Validador Estrito Quartz**:
  - Aceita 6 ou 7 campos: `Segundos`, `Minutos`, `Horas`, `Dia do Mês`, `Mês`, `Dia da Semana` e `Ano (opcional)`.
  - Validação estrita da regra de ouro do Quartz: ou `Dia do Mês` ou `Dia da Semana` **deve** conter o caractere `?`.
  - Suporte completo a caracteres especiais:
    - `/` (incrementos, ex: `0/15`)
    - `-` (intervalos, ex: `MON-FRI`, `9-17`)
    - `,` (listas de valores, ex: `1,15,30`)
    - `L` (último dia do mês ou última ocorrência de um dia da semana, ex: `L`, `LW`, `6L`)
    - `W` (dia de semana útil mais próximo, ex: `15W`)
    - `#` (n-ésimo dia da semana do mês, ex: `6#3` = 3ª sexta-feira do mês)
- **Gerador Visual Interativo**:
  - Abas intuitivas para cada componente da cron.
  - Sincronização bidirecional em tempo real: ao editar a caixa de texto, a interface se ajusta; ao selecionar opções nas abas, a expressão é gerada instantaneamente.
- **Tradução em Linguagem Natural (Português)**:
  - Explicação clara e imediata do comportamento agendado (ex: *"Às 10:15:00, de Segunda-feira a Sexta-feira"*).
- **Simulador de Próximas Execuções**:
  - Calcula em tempo real as próximas 5 datas/horas exatas de execução considerando o fuso horário local.
- **Presets Rápidos**:
  - Exemplos prontos com um clique (a cada 5 minutos, dias úteis às 09h, último dia do mês, 3ª sexta-feira, etc.).
- **Interface e Tema**:
  - Modo Escuro (padrão) e Modo Claro alternáveis no cabeçalho.
  - Botão de cópia rápida com feedback visual ("Copiado!").
  - Design responsivo para desktops, tablets e celulares.

---

## 📋 Estrutura dos Campos Quartz

| Posição | Campo | Obrigatório | Valores Permitidos | Caracteres Especiais |
|---|---|---|---|---|
| 1 | **Segundos** | Sim | `0-59` | `, - * /` |
| 2 | **Minutos** | Sim | `0-59` | `, - * /` |
| 3 | **Horas** | Sim | `0-23` | `, - * /` |
| 4 | **Dia do Mês** | Sim | `1-31` | `, - * ? / L W` |
| 5 | **Mês** | Sim | `1-12` ou `JAN-DEC` | `, - * /` |
| 6 | **Dia da Semana** | Sim | `1-7` (1=DOM, 7=SÁB) ou `SUN-SAT` | `, - * ? / L #` |
| 7 | **Ano** | Não | `1970-2099` | `, - * /` |

- **Zero dependências externas**: Não utiliza CDNs externos, fontes remotas ou imagens externas.
- **Total privacidade**: Nenhuma informação digitada sai do seu navegador.
- **Compatibilidade total**: Estruturado como documento XML/XHTML válido para máxima fidelidade e longevidade.
