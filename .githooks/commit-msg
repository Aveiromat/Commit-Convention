#!/bin/bash

# Define colors for output
RED='\033[0;31m'
GREEN='\033[0;32m'
YELLOW='\033[0;33m'
NC='\033[0m' # No Color

# Read the commit message
COMMIT_MSG_FILE=$1
COMMIT_MSG=$(cat "$COMMIT_MSG_FILE")

# Check if it's a merge commit, if so, allow it
if [[ "$COMMIT_MSG" =~ ^Merge.* ]]; then
  exit 0
fi

# Regex for our specific commit pattern: Emoji Type: Message
# Emojis are complex to match perfectly with standard bash regex, 
# so we look for any non-ASCII character (or specific emoji ranges) at the start,
# followed by a space, one of our types, a colon, a space, and text.
# Types allowed: feat|fix|docs|style|refactor|perf|test|build|ci|chore|cleanup|remove|raw|init

PATTERN="^[^a-zA-Z0-9[:space:]]+ (feat|fix|docs|style|refactor|perf|test|build|ci|chore|cleanup|remove|raw|init): .+$"

if [[ ! $COMMIT_MSG =~ $PATTERN ]]; then
  echo -e "${RED}ERRO: Mensagem de commit inválida!${NC}"
  echo -e "A mensagem não segue o padrão do ${YELLOW}COMMIT_CONVENTION.md${NC}."
  echo ""
  echo -e "Padrão esperado: ${GREEN}<Emoji> <tipo>: <descrição>${NC}"
  echo -e "Exemplo válido: ${GREEN}✨ feat: adiciona nova funcionalidade de login${NC}"
  echo ""
  echo "Tipos permitidos: feat, fix, docs, style, refactor, perf, test, build, ci, chore, cleanup, remove, raw, init"
  echo "Por favor, ajuste sua mensagem e tente novamente."
  exit 1
fi

exit 0
