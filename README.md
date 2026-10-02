# Achados e Perdidos UFRPE: Documento de Requisitos
> Atividade prática de Levantamento de Requisitos (ICC / UFRPE).
> Atividade de prática: não é entregue e não vale nota.
## 1. Equipe
| Nome | Curso |
|------|-------|
| Matheus | Ciência da Computação |
| Giovanna | Ciência da Computação |
| Jânio | Ciência da Computação |
| Francielly | Ciência da Computação |
| Jamilly | Ciência da Computação |
| Laura | Ciência da Computação |

## 2. Visão geral
**Problema:** objetos perdidos no campus da UFRPE ficam espalhados entre
portarias, secretarias e grupos de mensagem, e raramente voltam ao dono.
**Solução proposta:** <descrevam em 3 a 5 linhas o que a aplicação faz>
**Escopo:** <o que o sistema faz e o que ele NÃO faz. Ex.: não faz entregas>
## 3. Atores (usuários do sistema)
| Ator | Descrição | O que precisa fazer |
|------|-----------|---------------------|
| Estudante | Aluno com matrícula ativa | Procurar objetos, registrar perdas |
| Servidor | Professor ou técnico | <...> |
| Ponto de guarda | Portaria, biblioteca ou secretaria que guarda o objeto | <...> |
| Administrador | <...> | <...> |
## 4. Requisitos funcionais
Formato: código, nome, descrição, ator, prioridade e critérios de aceitação.
### RF01: Cadastrar objeto encontrado
- **Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Alta
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
### RF02: Buscar objetos
- **Descrição:** o sistema deve permitir buscar objetos por palavra-chave e
filtrar por categoria, campus/local e período.
- **Ator:** Todos
- **Prioridade:** Alta
- **Critérios de aceitação:**
- [ ] <...>
### RF03: Registrar objeto perdido
- **Descrição:** <...>
### RF04: Solicitar devolução (reivindicar objeto)
- **Descrição:** <como o dono prova que o objeto é dele?>
### RF05: Notificar possível correspondência
- **Descrição:** <avisar quem perdeu quando surgir um objeto parecido>
### RF06: Registrar entrega ao dono
### RF07: Autenticar usuário
### RF08: <novo requisito da equipe>
## 5. Requisitos não funcionais
| Código | Categoria | Requisito | Como medir |
|--------|-----------|-----------|------------|
| RNF01 | Usabilidade | Funcionar em celular e computador | Testar em telas de 360 px a 1920 px |
| RNF02 | Desempenho | Busca responde rápido | Resultado em até 2 segundos |
| RNF03 | Segurança | <...> | <...> |
| RNF04 | Privacidade (LGPD) | Não exibir dados pessoais de terceiros | <...> |
| RNF05 | Acessibilidade | <...> | <...> |
| RNF06 | Disponibilidade | <...> | <...> |
## 6. Regras de negócio
- **RN01:** Documentos oficiais (RG, CNH, cartão) não têm foto publicada;
aparecem só como "documento encontrado".
- **RN02:** Objetos não retirados em <N> dias são <doados / descartados>.
- **RN03:** A retirada exige <documento com foto / confirmação de detalhes>.
- **RN04:** <...>
## 7. Histórias de usuário
- Como **estudante**, quero **buscar meu casaco pela cor e pelo local**,
para **saber se alguém o encontrou sem ir a todas as portarias**.
- Como **vigilante da portaria**, quero **<...>**, para **<...>**.
- Como **<ator>**, quero **<ação>**, para **<benefício>**.
## 8. Dúvidas em aberto
- [ ] Quem pode acessar: só a comunidade UFRPE ou o público em geral?
- [ ] Os objetos ficam guardados em um só lugar ou em vários pontos?
- [ ] <...>
Modelo de README.md: copie p
