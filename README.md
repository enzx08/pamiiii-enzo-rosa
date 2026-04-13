# Criação de seu primeiro Expo!


**Precisaremos do seguinte para começar:**

-   [Expo Go](https://expo.dev/go) instalado em um dispositivo físico
-   [Node.js (versão LTS)](https://nodejs.org/en) instalado
-   [VS Code](https://code.visualstudio.com/) ou qualquer outro editor de código ou IDE preferido instalado
-   Um macOS, Linux ou Windows (PowerShell e [WSL2](https://expo.fyi/wsl) ) com uma janela de terminal aberta

  
## Inicializar um novo aplicativo Expo:

Usaremos [`create-expo-app`](https://docs.expo.dev/more/create-expo)para inicializar um novo aplicativo Expo. É uma ferramenta de linha de comando para criar um novo projeto React Native. Execute o seguinte comando no seu terminal:

>    #Create a project named StickerSmash

        
    npx create-expo-app@latest StickerSmash
    
   

>  #Navigate to the project directory

    
    -cd StickerSmash
#

Este comando criará um novo diretório de projeto chamado StickerSmash, usando o modelo padrão. Este modelo contém código boilerplate e bibliotecas essenciais para construir nosso aplicativo, incluindo o Expo Router. Continuaremos adicionando mais bibliotecas ao longo deste tutorial conforme necessário.

## Baixar ativos:
https://docs.expo.dev/static/images/tutorial/sticker-smash-assets.zip

1.  Descompacte o arquivo e substitua os ativos padrão no diretório your-project-name/assets/images .
2.  Abra o diretório do projeto em um editor de código ou IDE.

## Executar script reset-project:

Neste tutorial, criaremos nosso aplicativo do zero e entenderemos os fundamentos da adição de uma navegação baseada em arquivos. Vamos executar o `reset-project`script para remover o código padrão:

    - npm run reset-project
  
  Após executar o comando acima, restam dois arquivos ( index.tsx e _layout.tsx ) dentro do diretório app . Os arquivos anteriores do app e de outros diretórios ( components , constants e hooks — contendo código boilerplate) são movidos para dentro do diretório app-example pelo script. Criaremos nossos próprios diretórios e arquivos de componentes à medida que avançamos.
  
## Execute o aplicativo no celular e na web:
No diretório do projeto, execute o seguinte comando para iniciar o servidor de desenvolvimento no terminal:

    - npx expo start

Após executar o comando acima:

1.  O servidor de desenvolvimento será iniciado e você verá um código QR dentro da janela do terminal.
2.  Escaneie o código QR para abrir o aplicativo no dispositivo. No Android, use a opção Expo Go > Escanear código QR . No iOS, use o aplicativo de câmera padrão.
3.  Para executar o aplicativo web, pressione wno terminal. Isso abrirá o aplicativo web no navegador padrão.

Quando estiver em execução em todas as plataformas, o aplicativo deverá ficar assim:

![Aplicativo rodando em todas as plataformas](https://docs.expo.dev/static/images/tutorial/01-app-running-on-all-platforms.png)

#

## Editar a tela de índice:

O arquivo app/index.tsx define o texto exibido na tela do aplicativo. Ele é o ponto de entrada do nosso aplicativo e é executado quando o servidor de desenvolvimento é iniciado. Ele usa componentes principais do React Native, como `<View>`e `<Text>`para exibir o plano de fundo e o texto.

Os estilos aplicados a esses componentes usam objetos JavaScript em vez de CSS, que é usado na web. No entanto, muitas das propriedades parecerão familiares se você já usou CSS na web. A maioria dos componentes React Native aceita uma `style`propriedade que aceita um objeto JavaScript como valor. Para mais detalhes, consulte [Estilos no React Native](https://reactnative.dev/docs/style) .

Vamos modificar a tela app/index.tsx :

1.  Importe e crie um `StyleSheet`objeto para definir nossos estilos personalizados.`react-native``styles`
2.  Adicione uma `styles.container.backgroundColor`propriedade `<View>`com o valor de `#25292e`. Isso altera a cor de fundo.
3.  Substitua o valor padrão de `<Text>`por "Tela inicial".
4.  Adicione uma `styles.text.color`propriedade `<Text>`com o valor `#fff`(branco) para alterar a cor do texto.

# aplicativo/index.tsx:

```

    import { Text, View, StyleSheet } from 'react-native';
    
    export default function Index() {
      return (
        <View style={styles.container}>
          <Text style={styles.text}>Home screen</Text>
        </View>
      );
    }
    
    const styles = StyleSheet.create({
      container: {
        flex: 1,
        backgroundColor: '#25292e',
        alignItems: 'center',
        justifyContent: 'center',
      },
      text: {
        color: '#fff',
      },
    });

```

## Essa alteração será refletida automaticamente em todas as plataformas




