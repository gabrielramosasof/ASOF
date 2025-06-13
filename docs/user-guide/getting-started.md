# Primeiros Passos

## Pré-requisitos

Antes de começar, certifique-se de ter:

- Python 3.12 ou superior instalado
- pip ou uv (gerenciador de pacotes Python)
- Acesso à internet para download das dependências

## Instalação

1. Instale o ASOF via pip:
   ```bash
   pip install asof
   ```

   Ou usando uv:
   ```bash
   uv pip install asof
   ```

2. Verifique a instalação:
   ```bash
   python -c "import asof; print(asof.__version__)"
   ```

## Configuração Básica

1. Crie um arquivo de configuração `config.yaml`:
   ```yaml
   asof:
     environment: development
     debug: true
     database:
       url: sqlite:///local.db
   ```

2. Configure as variáveis de ambiente (opcional):
   ```bash
   export ASOF_ENV=development
   export ASOF_DEBUG=true
   ```

## Exemplo Rápido

```python
from asof import ASOF

# Inicialize o ASOF
app = ASOF()

# Configure sua aplicação
app.configure(config_path="config.yaml")

# Execute uma operação básica
result = app.process("exemplo")
print(result)
```

## Próximos Passos

- Explore mais [Funcionalidades](features.md)
- Consulte a [documentação da API](../api/overview.md)
- Veja exemplos práticos no [GitHub](https://github.com/seu-usuario/ASOF/examples)

## Solução de Problemas

Se encontrar algum problema durante a instalação ou configuração:

1. Verifique a versão do Python:
   ```bash
   python --version
   ```

2. Atualize o pip:
   ```bash
   python -m pip install --upgrade pip
   ```

3. Consulte nossa [página de solução de problemas](../dev-guide/troubleshooting.md)

## Suporte

Precisa de ajuda?
- Abra uma issue no GitHub
- Consulte nossa documentação
- Entre em contato com o suporte 