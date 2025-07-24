# python-scheduler-windows

Este repositório contém uma estrutura para agendar a execução de scripts Python em um runner Windows utilizando GitHub Actions.

## Estrutura

- `scripts/`: Coloque aqui seus scripts Python. Todos os arquivos `.py` nesse diretório serão executados pelo workflow agendado.
- `config/`: Contém arquivos de configuração. Por padrão inclui `settings.ini` de exemplo.
- `.github/workflows/`: Contém definições de workflows, como `schedule.yml` que agenda a execução.
- `requirements.txt`: Lista de dependências Python. Inicialmente vazio; adicione as dependências que seus scripts necessitam.

## Como funciona

O workflow `schedule.yml` é configurado para executar a cada 15 minutos em um runner **self-hosted** com etiqueta `windows`. Ele configura o ambiente Python, instala as dependências definidas em `requirements.txt` e executa todos os scripts presentes em `scripts/`.

Para utilizar, adicione seus scripts `.py` em `scripts/`, ajuste `requirements.txt` com as dependências necessárias, e configure `settings.ini` conforme sua necessidade.
