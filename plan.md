# Plano de Implementação - GrowUp Kids

## Estrutura da Aplicação (Single HTML File)

### Componentes Principais

1. **App Container**
   - Gestão de estado global
   - Navegação entre ecrãs

2. **Ecrã de Seleção de Avatar**
   - 6 avatares (3 femininos, 3 masculinos)
   - Filtro por género
   - Seleção e confirmação

3. **Dashboard Principal**
   - Informação do avatar selecionado
   - Estatísticas (moedas, XP, nível)
   - Árvore de plantas
   - Menu de navegação

4. **Sistema de Lições**
   - 25 lições de Literacia Financeira
   - 25 lições de Regras de Convivência
   - Progressão por idade (6, 7, 8+)
   - Texto-para-fala

5. **Sistema de Quiz**
   - Perguntas adaptativas
   - Feedback imediato
   - Recompensas (moedas, XP)

6. **Sistema de Desafios**
   - 10 desafios semanais
   - 9 tarefas domésticas

7. **Sistema de Gamificação**
   - Árvore de plantas (crescimento)
   - Moedas (GUC)
   - Barra de XP
   - Efeitos de confete

### Tecnologias (via CDN)

- React 18 (UMD)
- Babel Standalone (transpilação JSX)
- Framer Motion (animações)
- Canvas Confetti (celebrações)

### Armazenamento Local

```javascript
{
  selectedAvatar: {...},
  coins: 0,
  xp: 0,
  level: 1,
  plantStage: 0,
  completedLessons: [],
  completedChallenges: [],
  age: 6
}
```

## Conteúdo Educativo

### Literacia Financeira (25 lições)
1. O que é dinheiro?
2. Guardar moedas
3. Desejos vs Necessidades
4. Planeamento de gastos
5. Comparar preços
... (continuar até 25)

### Regras de Convivência (25 lições)
1. Cumprimentos e educação
2. Partilha e generosidade
3. Escuta ativa
4. Pedidos de desculpa
5. Respeito e diferenças
... (continuar até 25)
