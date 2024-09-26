
# **Media Queries no CSS**

Este repositório contém uma demonstração prática de como utilizar **Media Queries** no CSS para criar layouts responsivos e adaptados a diferentes dispositivos e orientações de tela. O projeto exemplifica o uso de regras específicas para impressão, tamanhos variados de dispositivos (smartphones, tablets, desktops) e para a disposição dos dispositivos (landscape e portrait).

### **Status do Projeto**

✅ **Projeto Concluído**

### **Pré-requisitos**

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com/), um navegador web para visualização e um editor de texto, como o [VSCode](https://code.visualstudio.com/).

### **🎲 Rodando o Projeto**

```bash
# Clone este repositório
$ git clone <https://github.com/KauaAlencar/POC-3-MediaQueries>

# Acesse a pasta do projeto no terminal/cmd
$ cd POC-3-MediaQueries

# Abra o arquivo index.html no seu navegador
# ou utilize uma extensão como Live Server no VSCode para rodar a aplicação.

```

### **Estrutura do Projeto**

O projeto é composto por uma página HTML (`index.html`) com um arquivo CSS embutido que demonstra como aplicar **Media Queries** de forma eficiente. Ele inclui exemplos de menus, galeria de imagens e layout em múltiplas colunas, adaptados para diferentes tamanhos de tela e orientações.

### **Conteúdo**

O projeto utiliza **Media Queries** para alterar a disposição de elementos como menus, galerias e textos dependendo das características do dispositivo.

| Recurso | Descrição |
| --- | --- |
| **Impressão** | O conteúdo é otimizado para ser impresso sem elementos visuais desnecessários, como cabeçalhos e rodapés. |
| **Tamanhos de Dispositivos** | Os layouts se ajustam para diferentes larguras, com menus e galerias sendo alterados dinamicamente para smartphone, tablet e desktop. |
| **Orientação (Landscape e Portrait)** | A cor do cabeçalho muda dependendo se o dispositivo está em modo paisagem (landscape) ou retrato (portrait). |

### **Descrição das Media Queries**

1. **Modo de Impressão**
    
    Utilizando a regra `@media print`, o layout é simplificado para impressão, removendo elementos visuais que não são relevantes ao serem impressos.
    
    ```css
    @media print {
        header, nav, footer {
            display: none;
        }
        .content {
            font-size: 12pt;
        }
    }
    ```
    
2. **Dispositivos de Diferentes Tamanhos**
    
    As media queries ajustam o layout para diferentes larguras de tela, alterando o design do menu e da galeria de imagens conforme o dispositivo:
    
    - Para **smartphones** (telas com largura de até 600px), o menu é disposto verticalmente e a galeria de imagens exibe uma única coluna.
    - Em **tablets** (entre 600px e 1024px), o menu permanece horizontal, mas a galeria exibe três colunas de imagens.
    - Nos **desktops** (mais de 1024px), o layout exibe quatro colunas na galeria de imagens.
    
    ```css
    @media (max-width: 600px) {
        .gallery {
            grid-template-columns: 1fr;
        }
    }
    @media (min-width: 600px) and (max-width: 1024px) {
        .gallery {
            grid-template-columns: 1fr 1fr 1fr;
        }
    }
    @media (min-width: 1024px) {
        .gallery {
            grid-template-columns: 1fr 1fr 1fr 1fr;
        }
    }
    ```
    
3. **Orientação de Tela (Landscape e Portrait)**
    
    Dependendo da orientação do dispositivo, a cor do cabeçalho muda, utilizando as media queries para `landscape` e `portrait`:
    
    ```css
    @media (orientation: landscape) {
        header {
            background-color: #28a745;
        }
    }
    @media (orientation: portrait) {
        header {
            background-color: #ffc107;
        }
    }
    ```

### **Exemplo de Saída**

- **Smartphones**: Menu vertical, galeria de imagens em uma coluna, texto em uma única coluna.
- **Tablets**: Menu horizontal, galeria com três colunas, texto em duas colunas.
- **Desktops**: Menu horizontal, galeria com quatro colunas, texto em três colunas.
- **Impressão**: Layout otimizado sem cabeçalho e rodapé.
- **Orientação de Tela**: Cabeçalho verde em modo paisagem e amarelo em modo retrato.

### **Colaboradores**
<table>
  <tr>
    <td align="center"><a href="https://github.com/KauaAlencar"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/172075258?v=4" width="100px;" alt=""/><br /><sub><b>Kauã Alencar</b></sub></a><br /><a href="https://www.linkedin.com/in/kau%C3%A3-alencar-b15119215/" title="Linkedin">🚀</a></td>
    <td align="center"><a href="https://github.com/GuilhermeShinohara"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/180458966?v=4" width="100px;" alt=""/><br /><sub><b>Guilherme Shinohara</b></sub></a><br /><a href="https://github.com/GuilhermeShinohara" title="GitHub">🚀</a></td>
    <td align="center"><a href="https://github.com/LeoFavaron"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/179886009?v=4" width="100px;" alt=""/><br /><sub><b>Leonardo Favaron</b></sub></a><br /><a href="https://github.com/LeoFavaron" title="GitHub">🚀</a></td>
  </tr>
</table>

### **📝 Licença**

Este projeto está sob a licença MIT.
