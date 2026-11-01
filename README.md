# Complementos do Noch

Distribuição pública dos pacotes opcionais do Noch. O código-fonte da aplicação permanece privado e não é enviado para este repositório.

## Lagroll para Windows x64

Tradutor de tela offline, de inglês para português brasileiro. No Noch, ative **Lagroll** em **Configurações avançadas → Complementos**. A aba oferece **Tradução contínua** e **Traduzir uma vez**. Desativar encerra o tradutor e remove os arquivos baixados.

- Versão do pacote: 1 (protocolo 1).
- Download: 299.886.365 bytes (aproximadamente 300 MB).
- Arquivos instalados: 638.860.555 bytes (aproximadamente 639 MB).
- Requer Windows x64 e o Microsoft Visual C++ Redistributable 2015–2022 x64.
- O pacote inclui o auxiliar, runtime .NET, Python, OCR, modelo de tradução e avisos/licenças. Não inclui perfis, capturas pessoais ou código-fonte do Noch.
- As capturas e o texto reconhecido são processados localmente.

[Baixar Lagroll v1](https://github.com/c00rvus/noch-addons/releases/download/addon-lagroll-1/lagroll-noch-win-x64-v1.zip)

SHA-256:

```text
6ee782f1cb22adc8016fa85b113150f22eb674f92b75bc6a7a6c5b1a76988ba9
```

O Noch verifica o tamanho e o SHA-256 antes da instalação. Os endereços de cada versão são fixos; atualizações do complemento usam uma nova versão. Estes pacotes não habilitam o atualizador da aplicação nem usam o feed do Oyenza.

## Ditar para Windows x64

Ditado offline em português com Whisper large-v3-turbo Q5_0. Ative **Ditar** em **Configurações avançadas → Complementos**. Use **Ctrl+Alt+D** para iniciar/parar ou **Ctrl+Alt+Espaço** para segurar e falar; há botões equivalentes na aba. A transcrição começa ao parar/soltar, retorna ao campo original quando disponível e fica no histórico local das últimas 30 transcrições.

- Versão do pacote: 1; execução nativa Whisper CLI, independente do protocolo JSON-lines do Lagroll.
- Download: 550.155.634 bytes (aproximadamente 550 MB).
- Arquivos instalados: 636.837.149 bytes (aproximadamente 637 MB).
- Requer Windows x64 e Microsoft Visual C++ x64 runtime; inclui aceleração CPU/OpenBLAS e fallback para CPU.
- Modelo e runtime são carregados somente ao transcrever; o processo encerra ao concluir. Não requer Codex, conta, Python, PyTorch ou transcrição em nuvem.
- Preserva as licenças MIT, OpenBLAS BSD e LAPACK. Não contém código-fonte do Noch, perfis, histórico ou gravações pessoais.

[Baixar Ditar v1](https://github.com/c00rvus/noch-addons/releases/download/addon-dictation-1/dictation-whisper-turbo-q5-win-x64-v1.zip)

SHA-256:

```text
e8747cccd463dc622ef115cf0d4ef0719b81ccf514fc05ab3d3c3a5d49e8f9fc
```

## Aceleração GPU do Ditar (Vulkan, Windows x64)

Recurso nativo adicional para versões do Noch com suporte à aceleração Vulkan. Ao ativar **Ditar**, o Noch baixa este runtime sob demanda e verifica seu tamanho e SHA-256. Ele usa o mesmo modelo Q5 do pacote base: não inclui nem baixa outra cópia dos pesos.

- Versão do recurso: 1; pertence ao Ditar e não adiciona outra aba ou switch de complemento.
- Download adicional: 16.557.835 bytes (aproximadamente 16,6 MB).
- Arquivos instalados adicionais: 51.865.473 bytes (aproximadamente 51,9 MB).
- Requer Windows x64 com UCRT e driver gráfico Vulkan compatível. Nenhum driver, SDK ou compilador acompanha o ZIP.
- Usa a GPU quando disponível; o runtime CPU/OpenBLAS do pacote base permanece como fallback.
- Durante o download opcional, o ditado já pode usar a CPU. Falhas no acelerador não desativam o Ditar; uma nova ativação permite tentar novamente.
- O helper inicia somente ao transcrever e encerra ao terminar. Desativar Ditar remove também este recurso.
- Contém o runtime whisper.cpp/ggml e suas dependências nativas, proveniência e licenças. Não contém modelo, código privado do Noch, perfil, histórico ou áudio pessoal.

[Baixar aceleração Vulkan v1](https://github.com/c00rvus/noch-addons/releases/download/addon-dictation-vulkan-1/dictation-vulkan-win-x64-v1.zip)

SHA-256:

```text
727544eb069de37b404be321842b368b7a9d1d1d3f46d9f1acd9100af4ab8ea9
```

## Licenças e créditos

Os avisos, licenças e atribuições dos componentes acompanham o respectivo ZIP: conforme o complemento, .NET/WPF, Python, bibliotecas de OCR e tradução, modelos, whisper.cpp/ggml, LLVM e headers Vulkan/SPIR-V. A atribuição CC-BY 4.0 do modelo de tradução está em models/en-pb/README.md dentro do pacote. Consulte esses arquivos para as condições de cada componente.