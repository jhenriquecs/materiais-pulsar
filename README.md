# Materiais Pulsar

Materiais da oficina:

- **material-aula.zip** — arquivos da aula (textos, imagens e estilo).
- **quarto.deb** — instalador do [Quarto](https://quarto.org) 1.10.19 para Linux (Ubuntu/Debian, 64 bits).

## 1. Baixar os arquivos

### Pelo navegador

- Material da aula: [material-aula.zip](https://github.com/jhenriquecs/materiais-pulsar/raw/main/material-aula.zip)
- Quarto: [quarto.deb](https://github.com/jhenriquecs/materiais-pulsar/releases/latest/download/quarto.deb)

Os arquivos vão para a pasta **Downloads**.

> O `quarto.deb` fica na aba [Releases](https://github.com/jhenriquecs/materiais-pulsar/releases) porque é grande demais para ficar junto dos outros arquivos.

### Pelo terminal

Abra o terminal (`Ctrl` + `Alt` + `T`) e rode:

```bash
cd ~/Downloads
wget https://github.com/jhenriquecs/materiais-pulsar/raw/main/material-aula.zip
wget https://github.com/jhenriquecs/materiais-pulsar/releases/latest/download/quarto.deb
```

## 2. Instalar o Quarto

No terminal, entre na pasta onde o arquivo foi baixado e instale com o `apt`:

```bash
cd ~/Downloads
sudo apt install ./quarto.deb
```

Digite sua senha quando ela for pedida (nada aparece enquanto você digita, é normal) e confirme com `S` ou `Y` se o `apt` perguntar.

> Atenção ao `./` antes do nome do arquivo. Sem ele, o `apt` procura um pacote chamado `quarto.deb` na internet e dá erro.

Para conferir se deu certo:

```bash
quarto --version
```

Deve aparecer `1.10.19`.

## 3. Descompactar o material da aula

```bash
cd ~/Downloads
unzip material-aula.zip -d material-aula
```

Se o `unzip` não estiver instalado: `sudo apt install unzip`. Também dá para clicar com o botão direito no arquivo e escolher **Extrair aqui**.

## Desinstalar o Quarto

```bash
sudo apt remove quarto
```
