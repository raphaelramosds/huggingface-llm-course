# Poetry: instalação e configuração

## Instalação

```shell
# Instalação de pacotes do Linux
sudo apt-get install git make python3 ffmpeg

# Instalação do poetry
curl -sSL https://install.python-poetry.org | python3 -

# NOTE: Apos executar o comando abaixo, adicione-o ao .zshrc ou .bashrc
export PATH="/home/$USER/.local/bin:$PATH:"
```

## Configuração do projeto (opcional)

Esse passo é útil caso queira configurar as dependências do Poetry do zero

```shell
# Adicionar fonte do PyTorch aos índices do Poetry
poetry source add --priority explicit pytorch_cpu https://download.pytorch.org/whl/cpu

# Adicionar e instalar dependencias
poetry add --source pytorch_cpu torch "transformers[sentencepiece]" ipykernel Pillow ffmpeg ffmpeg-python

# Instalar dependencias
poetry install
```