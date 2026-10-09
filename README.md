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
**Problema:** Todos os dias, objetos perdidos no campus da UFRPE, das mais diversas naturezas, ficam espalhados entre
portarias, secretarias e grupos de mensagem, e raramente voltam ao dono.

**Solução proposta:** Um sistema centralizado de Achados e Perdidos da UFRPE onde a comunidade acadêmica pode registrar itens encontrados e buscar por pertences perdidos, conectando os pontos de guarda aos dono, com os materiais complementares disponíveis [aqui](https://yokoapps.com.br/computacao).

**Escopo:** O sistema gerencia o registro, a busca e a notificação de itens perdidos e encontrados. O sistema não faz entregas ou transporte físico dos objetos.

## 3. Atores (usuários do sistema)
| Ator | Descrição | O que precisa fazer |
|------|-----------|---------------------|
| Estudante | Aluno com matrícula ativa | Procurar objetos, registrar perdas. |
| Servidor | Professor ou técnico | Procurar objetos, registrar perdas ou itens encontrados. |
| Ponto de guarda | Portaria, biblioteca ou secretaria que guarda o objeto | Confirmar a entrega, guardar fisicamente o objeto. |
| Administrador | Coordenador de curso | Responsável por gerenciar as categorias da plataforma, moderar registros e lidar com itens expirados. |
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
**Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Alta
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
### RF04: Solicitar devolução (reivindicar objeto)
**Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Alta
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
### RF05: Notificar possível correspondência
**Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Média
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
### RF06: Registrar entrega ao dono
**Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Alta
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
### RF07: Autenticar usuário
**Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Alta
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
### RF08: Buscar item perdido por categoria/data
**Descrição:** o sistema deve permitir que um usuário registre um objeto
encontrado, informando categoria, descrição, cor, local, data e foto (opcional).
- **Ator:** Estudante, Servidor, Ponto de guarda
- **Prioridade:** Baixa
- **Critérios de aceitação:**
- [ ] Os campos categoria, local e data são obrigatórios.
- [ ] O objeto aparece na busca logo após ser salvo.
- [ ] O sistema informa em qual ponto de guarda o objeto deve ser deixado.
## 5. Requisitos não funcionais
| Código | Categoria | Requisito | Como medir |
|--------|-----------|-----------|------------|
| RNF01 | Usabilidade | Funcionar em celular e computador | Testar em telas de 360 px a 1920 px |
| RNF02 | Desempenho | Busca responde rápido | Resultado em até 2 segundos |
| RNF03 | Segurança | <...> | <...> |
| RNF04 | Privacidade (LGPD) | Não exibir dados pessoais de terceiros | Restringir o acesso dos dados aos administradores |
| RNF05 | Acessibilidade | Interface user-friendly | Botões e caixas de entrada simples |
| RNF06 | Disponibilidade | Funcionar no horário da UFRPE | Permitir operações de 6h às 22h |
| RNF07 | <...> | <...> | <...> | 
## 6. Regras de negócio
- **RN01:** Documentos oficiais (RG, CNH, cartão) não têm foto publicada;
aparecem só como "documento encontrado".
- **RN02:** Objetos não retirados em 60 dias são <doados / descartados>.
- **RN03:** A retirada exige documento com foto e um dos seguintes: nota fiscal, extrato de compra, foto com o objeto.
- **RN04:** 
## 7. Histórias de usuário
- Como **estudante**, quero **buscar meu casaco pela cor e pelo local**,
para **saber se alguém o encontrou sem ir a todas as portarias**.
- Como **vigilante da portaria**, quero **<...>**, para **que não me enchem o saco**.
- Como **secretária do departamento**, quero **<ação>**, para **<benefício>**.
## 8. Dúvidas em aberto
- [ ] Quem pode acessar: só a comunidade UFRPE ou o público em geral?
- [ ] Os objetos ficam guardados em um só lugar ou em vários pontos?
- [ ] 
