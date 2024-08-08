# AI

ollama 사용으로 llm 환경 구성

## 백엔드 설정용 터미널 명령어 - 개발자용
curl -fsSL https://ollama.com/install.sh | sh
pip install huggingface-hub
huggingface-cli download \
  chatpdflocal/llama3.1-8b-gguf \
  ggml-model-Q4_K_M.gguf \
  --local-dir 본인의_컴퓨터_프로젝트_경로 \
  —local-dir-use-symlinks False
ollama create review_dev -f model/review_dev
ollama run review_dev

## 백엔드 설정용 터미널 명령어 - 비개발자용
curl -fsSL https://ollama.com/install.sh | sh
pip install huggingface-hub
huggingface-cli download \
  chatpdflocal/llama3.1-8b-gguf \
  ggml-model-Q4_K_M.gguf \
  --local-dir 본인의_컴퓨터_프로젝트_경로 \
  —local-dir-use-symlinks False
ollama create revew_nondev -f model/review_dev
ollama run review_nondev
