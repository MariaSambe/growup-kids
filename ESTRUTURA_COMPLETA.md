# Estrutura Completa - GrowUp Kids Surreal

## Arquitetura da Aplicação

### Ecrãs/Views

1. **Loading Screen** ✅ (já implementado)
2. **Seleção de Avatar** ✅ (já implementado)
3. **Confirmação de Avatar** ✅ (já implementado)
4. **Dashboard Cósmico** 🔨 (a implementar)
5. **Biblioteca de Lições** 🔨 (a implementar)
6. **Quiz Interativo** 🔨 (a implementar)
7. **Desafios Semanais** 🔨 (a implementar)
8. **Tarefas Domésticas** 🔨 (a implementar)
9. **Perfil do Utilizador** 🔨 (a implementar)

### Componentes Principais

#### 1. Dashboard Cósmico
- **Estatísticas do utilizador** (moedas, XP, nível, streak)
- **Planta 3D** que cresce com o progresso
- **Barra de XP** animada com efeitos de partículas
- **Menu de navegação** flutuante
- **Conquistas recentes** com animações
- **Próxima lição** em destaque

#### 2. Sistema de Gamificação
- **Moedas (GrowCoins)**: Ganhas ao completar lições
- **XP (Experiência)**: Acumula para subir de nível
- **Níveis**: 1-50 (cada nível = 100 XP)
- **Streak**: Dias consecutivos de aprendizagem
- **Conquistas**: Badges especiais por marcos
- **Planta Virtual**: 10 estágios de crescimento

#### 3. Biblioteca de Lições (50 lições)

**Literacia Financeira (25 lições):**

*Nível Iniciante (6-8 anos):*
1. O que é dinheiro?
2. Moedas e notas
3. Poupar vs Gastar
4. Mealheiro mágico
5. Comprar com sabedoria
6. Necessidades vs Desejos
7. Ganhar dinheiro
8. Valor das coisas

*Nível Intermédio (9-11 anos):*
9. O que é um banco?
10. Conta poupança
11. Orçamento básico
12. Mesada inteligente
13. Comparar preços
14. Publicidade e marketing
15. Dinheiro digital
16. Cartões de débito

*Nível Avançado (12-14 anos):*
17. Juros e poupança
18. Investimento básico
19. Ações e empresas
20. Risco e recompensa
21. Crédito e empréstimos
22. Impostos básicos
23. Empreendedorismo
24. Planeamento financeiro
25. Economia familiar

**Regras de Convivência (25 lições):**

*Em Casa:*
1. Respeitar os pais
2. Ajudar nas tarefas
3. Partilhar com irmãos
4. Cuidar dos animais
5. Organizar o quarto
6. Horários e rotinas
7. Comunicação familiar
8. Resolver conflitos

*Na Escola:*
9. Respeitar professores
10. Ser bom colega
11. Trabalho em equipa
12. Não fazer bullying
13. Pedir ajuda
14. Partilhar materiais
15. Seguir regras
16. Ser pontual

*Em Sociedade:*
17. Boas maneiras
18. Respeitar diferenças
19. Ajudar os outros
20. Cuidar do ambiente
21. Segurança online
22. Privacidade
23. Honestidade
24. Responsabilidade
25. Empatia e bondade

#### 4. Sistema de Quiz
- **3-5 perguntas** por lição
- **4 opções** de resposta
- **Feedback imediato** com confetti ou animação
- **Explicação** da resposta correta
- **Pontuação**: 10 moedas + 20 XP por lição completa
- **Efeitos sonoros** e visuais

#### 5. Desafios Semanais (10 desafios)
1. Poupar 5 moedas esta semana
2. Ajudar em 3 tarefas domésticas
3. Completar 5 lições
4. Fazer um orçamento semanal
5. Pesquisar preços de 3 produtos
6. Criar um plano de poupança
7. Ensinar algo a alguém
8. Praticar boas maneiras
9. Cuidar do ambiente
10. Ser gentil 7 dias seguidos

#### 6. Tarefas Domésticas (9 tarefas)
1. Arrumar o quarto
2. Lavar a loiça
3. Pôr a mesa
4. Regar plantas
5. Dar comida aos animais
6. Dobrar roupa
7. Aspirar o chão
8. Limpar a secretária
9. Ajudar a cozinhar

### Dados e Estado

```javascript
const userState = {
  // Perfil
  avatar: {
    name: "Sofia Génio",
    emoji: "👧🎀",
    color: "#ff69b4"
  },
  
  // Progresso
  coins: 0,
  xp: 0,
  level: 1,
  streak: 0,
  
  // Lições
  completedLessons: [],
  currentLesson: null,
  
  // Planta
  plantStage: 0, // 0-10
  
  // Desafios
  weeklyChallenge: null,
  completedChallenges: [],
  
  // Tarefas
  completedChores: [],
  
  // Conquistas
  achievements: []
}
```

### Estilo Visual Surreal (mantido em tudo)

- **Fundo 3D** com partículas em todas as views
- **Glassmorphism** em todos os cards
- **Animações GSAP** em todas as transições
- **Confetti** em todas as celebrações
- **Cursor mágico** em toda a aplicação
- **Efeitos de hover** em todos os botões
- **Glow effects** em elementos importantes

### Navegação

```
Loading → Seleção Avatar → Dashboard
                              ↓
                    ┌─────────┼─────────┐
                    ↓         ↓         ↓
                Lições    Desafios   Perfil
                    ↓
                  Quiz
                    ↓
              (volta ao Dashboard)
```

### Persistência de Dados

- **localStorage** para guardar progresso
- **Chave**: `growup_kids_user_data`
- **Formato**: JSON
- **Backup**: Exportar/Importar progresso

## Implementação

### Fase 1: Dashboard
- Layout com menu lateral
- Estatísticas animadas
- Planta 3D com SVG/Canvas
- Barra de XP com efeitos

### Fase 2: Lições e Quiz
- Todas as 50 lições com conteúdo
- Sistema de perguntas e respostas
- Feedback visual e sonoro
- Progressão e desbloqueio

### Fase 3: Desafios e Tarefas
- Lista de desafios semanais
- Sistema de check-in
- Tarefas domésticas
- Recompensas

### Fase 4: Polimento
- Animações finais
- Sons e música
- Otimizações
- Testes completos
