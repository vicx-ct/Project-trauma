OpenDeX — Etapa 1

Um protótipo de interface desktop para Android, desenvolvido com Kotlin e Jetpack Compose.

O OpenDeX é um projeto experimental que implementa uma interface inspirada em ambientes desktop, executada como um aplicativo Android comum. Seu objetivo nesta primeira etapa é estabelecer uma área de trabalho funcional, com acesso a aplicativos instalados, barra de tarefas, configurações e informações do dispositivo.

O projeto utiliza APIs públicas do Android e componentes do ecossistema Jetpack Compose.

Funcionalidades implementadas no código

- Área de trabalho: tela principal com fundo em gradiente.
- Barra de tarefas: acesso ao menu iniciar, configurações e aplicativos abertos recentemente pelo próprio OpenDeX.
- Menu iniciar: lista aplicativos iniciáveis detectados no dispositivo, com campo de pesquisa.
- Inicialização de aplicativos: abre aplicativos selecionados utilizando os mecanismos normais do Android.
- Bandeja do sistema: apresenta horário, percentual da bateria, estado de carregamento e conectividade Wi-Fi.
- Configurações: alternância entre temas claro e escuro e controle de animações.
- Persistência de preferências: utiliza DataStore para salvar configurações entre execuções.
- Diagnóstico do dispositivo: consulta recursos relacionados a janelas, Picture-in-Picture, telas secundárias e monitores conectados.
- Detecção do Winlator: verifica se o pacote conhecido "com.winlator" está instalado e identifica esse aplicativo visualmente no menu.
- Relatório de diagnóstico: permite copiar as informações coletadas para análise posterior.
- Suporte à interface com teclado e mouse: utiliza componentes padrão do Android e do Compose.
- Redimensionamento da própria Activity: declara suporte a redimensionamento quando permitido pelo sistema e pelo fabricante.

Tecnologias

- Kotlin
- Jetpack Compose
- Android SDK
- AndroidX
- Material 3
- Material Symbols por meio da biblioteca de ícones do Compose
- Kotlin Coroutines e Flow
- DataStore Preferences
- Gradle com Kotlin DSL

Como funciona

A aplicação utiliza uma Activity principal para hospedar a interface desktop. Os componentes de interface são desenvolvidos com Jetpack Compose, enquanto classes separadas consultam os aplicativos instalados, o estado do sistema, as preferências e as capacidades de exibição do dispositivo.

A abertura de aplicativos é realizada por meio de Intents do Android. As informações de diagnóstico são consultadas nas APIs disponíveis, em vez de serem apresentadas como capacidades presumidas do aparelho.

Limitações desta etapa

Esta versão ainda não implementa janelas próprias ao redor de aplicativos de terceiros. Os aplicativos iniciados pelo menu são abertos normalmente pelo Android, e a barra de tarefas mantém atalhos para aplicativos recentes, não um sistema completo de gerenciamento de janelas.

Também não estão implementados nesta etapa:

- Transmissão de tela por Miracast.
- Explorador de arquivos integrado.
- Execução de arquivos EXE.
- Alteração da resolução global ou do DPI do Android.
- Um ambiente Linux integrado.
- Um sistema próprio de janelas flutuantes para aplicativos externos.

O redimensionamento declarado no Manifest aplica-se à Activity do OpenDeX quando o sistema oferece suporte; não garante que aplicativos externos possam ser redimensionados livremente.

Compilação

O projeto foi preparado para Android Studio, mas o ZIP informa que ainda não foi compilado nem validado em um dispositivo físico.

O repositório inclui um workflow do GitHub Actions destinado à compilação de um APK de depuração. A compilação depende da configuração correta do Gradle, das dependências e do ambiente Android.

Estado do projeto

Etapa 1 — protótipo inicial.

O código contém a implementação inicial da interface e dos recursos descritos neste documento. A compilação, a instalação e os testes em dispositivos reais continuam necessários para confirmar o funcionamento.

O OpenDeX é um projeto independente e experimental, sem afiliação oficial à Samsung ou a outros fabricantes.
