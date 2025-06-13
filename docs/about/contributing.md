# Guia de Contribuição

## Como Contribuir

Agradecemos seu interesse em contribuir com o ASOF! Este guia ajudará você a entender nosso processo de contribuição.

## Código de Conduta

Este projeto segue um Código de Conduta. Ao participar, você concorda em seguir suas diretrizes.

## Processo de Contribuição

### 1. Preparando o Ambiente

1. Faça um fork do repositório
2. Clone seu fork:
   ```bash
   git clone https://github.com/seu-usuario/ASOF.git
   cd ASOF
   ```

3. Configure o ambiente de desenvolvimento:
   ```bash
   python -m venv venv
   source venv/bin/activate  # No Windows: venv\Scripts\activate
   pip install -e ".[dev]"
   ```

### 2. Fazendo Alterações

1. Crie uma branch para sua feature:
   ```bash
   git checkout -b feature/nome-da-feature
   ```

2. Faça suas alterações seguindo as convenções de código

3. Execute os testes:
   ```bash
   pytest
   ```

4. Atualize a documentação se necessário

### 3. Enviando Contribuições

1. Commit suas alterações:
   ```bash
   git add .
   git commit -m "feat: adiciona nova funcionalidade"
   ```

2. Push para seu fork:
   ```bash
   git push origin feature/nome-da-feature
   ```

3. Abra um Pull Request

## Convenções de Código

### Estilo de Código

- Siga a PEP 8
- Use type hints
- Documente funções e classes
- Mantenha o código em português

### Commits

Seguimos o padrão Conventional Commits:

- `feat:` nova funcionalidade
- `fix:` correção de bug
- `docs:` alterações na documentação
- `test:` adição ou modificação de testes
- `refactor:` refatoração de código
- `style:` formatação de código
- `chore:` alterações em arquivos de build

### Testes

- Escreva testes para novas funcionalidades
- Mantenha a cobertura de testes alta
- Use pytest para testes

## Revisão de Código

- Seu PR será revisado por pelo menos um mantenedor
- Feedback será dado em até 5 dias úteis
- Pode ser solicitado alterações

## Reportando Bugs

Use o template de issue para bugs:

```markdown
**Descrição do Bug**
Uma descrição clara do bug

**Como Reproduzir**
1. Passo 1
2. Passo 2
3. ...

**Comportamento Esperado**
O que deveria acontecer

**Screenshots**
Se aplicável

**Ambiente**
- OS: [ex: Ubuntu 20.04]
- Python: [ex: 3.12.0]
- ASOF: [ex: 1.0.0]
```

## Sugerindo Melhorias

Use o template de feature request:

```markdown
**Problema**
Descrição do problema que sua sugestão resolve

**Solução Proposta**
Como você sugere resolver

**Alternativas Consideradas**
Outras soluções que você considerou

**Contexto Adicional**
Qualquer outro contexto relevante
```

## Licença

Ao contribuir, você concorda que suas contribuições serão licenciadas sob a mesma licença do projeto. 