# 🛡️ Padrões de commits e Validador (Git Hook) 📜

Este repositório é uma **ferramenta auxiliar** criada para ser utilizada em vários tipos de projetos. Ele contém:
1. Um script `commit-msg` (Git Hook personalizado) para garantir que qualquer projeto siga estritamente o padrão de **Conventional Commits com Emojis**.
2. A documentação completa das regras no arquivo `COMMIT_CONVENTION.md`.

## 📖 Regras de Commits

Para conferir todas as regras, tipos de commits (feat, fix, chore, etc.), lista de emojis e comandos úteis do Git, consulte o documento oficial:

👉 **[Ler as Regras de Commits (COMMIT_CONVENTION.md)](./.githooks/COMMIT_CONVENTION.md)**

---

## 🛠️ Como utilizar este repositório em OUTROS Projetos Novos

Como este é um repositório auxiliar, o objetivo é levar a pasta `.githooks` para os seus novos projetos e configurá-lo para validar as mensagens de commit localmente.

### Passo 1: Obtenha os arquivos 📂

Copie a pasta `.githooks` deste repositório para a raiz do seu novo projeto. Tudo que é necessário (script e documentação) está dentro dela.

Por exemplo:
```bash
# Clone este repositório auxiliar em algum lugar
git clone https://github.com/Aveiromat/Commit-Convention.git

# Copie a pasta de hooks para a raiz do seu projeto novo
cp -r Commit-Convention/.githooks /caminho/para/seu/novo-projeto/
```

### Passo 2: Configure o projeto seguindo as instruções ⚙️

As instruções de como ativar o verificador no seu novo repositório (junto com a documentação de `feat`, `fix`, emojis, etc.) estão detalhadas dentro do README da própria pasta de configuração.

👉 **[Ler as instruções e Regras de Commits](./.githooks/README.md)**

---

> **Nota:** Commits automáticos de Merge (ex: `Merge branch...`) são ignorados para não impactar o fluxo de trabalho do Git.
