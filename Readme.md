## Sobre o Projeto

Este projeto visa a disponibilização de um conjunto de Snippets ou atalhos para criação de componentes e arquivos de configuração em aplicações React Native visando a utilização de React Hooks, logo, apenas Stateless Components são criados.

## Começando

![Create React Native Component](./images/example.gif)

## Linguagens suportadas (extensões de arquivo)

- JavaScript (.js)
- React Native (.js)
- Typescript React Native (.tsx)

## Snippets

Abaixo segue a lista com todos os Snippets disponíveis e os gatilhos para cada um. O **⇥** significa a tecla `TAB`.

## React-hooks

|           Gatilho | Conteúdo                             |
| ----------------: | ------------------------------------ |
|    `state-hook →` | `const [$1, set$1] = useState($2)`   |
|      `cdm-hook →` | `useEffect(() => { $0 }, []);`       |
| `cdupdate-hook →` | `useEffect(() => { $0 });`           |
| `cwumount-hook →` | `useEffect(() => () => { $0 }, []);` |

## Imports e exports

|                    Gatilho | Conteúdo                             |
| -------------------------: | ------------------------------------ |
|         `import default →` | `import $2 from '${1}';`             |
| `import react statement →` | `import React, { $1 } from 'react';` |
|       `import statement →` | `import { $2 } from '$1';`           |
|         `export default →` | `export default $1`                  |
|        `export function →` | `export const $1 = ($2) => { };`     |

## Métodos básicos

|              Gatilho | Conteúdo                          |
| -------------------: | --------------------------------- |
|         `const {} →` | `const { $0 } = $1';`             |
|           `let {} →` | `let { $0 } = $1;`                |
|   `function arrow →` | `const $1 = ($2)=>{ $0 };`        |
|             `()=> →` | `($1)=>{ $0 }`                    |
| `function default →` | `const $1 = function($2) { $0 };` |

## Console

|          Gatilho | Conteúdo                   |
| ---------------: | -------------------------- |
|  `csl default →` | `console.log('$0');`       |
| `csl variable →` | `console.log('$1: ', $1);` |

## Styles

|                     Gatilho | Conteúdo                     |
| --------------------------: | ---------------------------- |
|          `justifyContent →` | `justifyContent: '',`        |
|              `alignItems →` | `alignItems: '',`            |
|               `alignSelf →` | `alignSelf: '',`             |
|            `alignContent →` | `alignContent: '',`          |
|             `borderWidth →` | `borderWidth: ,`             |
|             `borderColor →` | `borderColor: ,`             |
|            `borderRadius →` | `borderRadius: ,`            |
|  `borderBottomLeftRadius →` | `borderBottomLeftRadius: ,`  |
| `borderBottomRightRadius →` | `borderBottomRightRadius: ,` |
|     `borderTopLeftRadius →` | `borderTopLeftRadius: ,`     |
|    `borderTopRightRadius →` | `borderTopRightRadius: ,`    |
|         `backgroundColor →` | `backgroundColor: ,`         |
|                 `display →` | `display: ,`                 |
|                 `opacity →` | `opacity: ,`                 |
|                    `flex →` | `flex: '',`                  |
|           `flexDirection →` | `flexDirection: '',`         |
|                `fontSize →` | `fontSize: '',`              |
|              `fontWeight →` | `fontWeight: '',`            |
|                  `height →` | `height: ,`                  |
|                   `width →` | `width: ,`                   |
|                  `margin →` | `margin: ,`                  |
|            `marginBottom →` | `marginBottom: ,`            |
|        `marginHorizontal →` | `marginHorizontal: ,`        |
|              `marginLeft →` | `marginLeft: ,`              |
|             `marginRight →` | `marginRight: ,`             |
|               `marginTop →` | `marginTop: ,`               |
|          `marginVertical →` | `marginVertical: ,`          |
|                 `padding →` | `padding: ,`                 |
|                `position →` | `position: absolute,`        |
|                    `left →` | `left: '',`                  |
|                   `right →` | `right: '',`                 |
|                     `top →` | `top: '',`                   |
|                  `bottom →` | `bottom: '',`                |

### `shadow elevation` Define um estilo de sombra

```js
shadowColor: ${1:'#000'},
shadowOffset: {
  width: ${2:0},
  height: ${3:2},
},
shadowOpacity: ${4:0.25},
shadowRadius: ${5:3.84},
elevation: ${6:5},
$0
```

## React Native Components - Javascript

### `rnc` Cria um Componente **Stateless**

```javascript
import React from 'react';
import { View, Text } from 'react-native';

// import styles from './styles'

const $1 = props => {
  return (
    <View>
      <Text>$1 Component</Text>
    </View>
  );
};

export default $1;
```

### `rnc-redux` Cria um Componente **Stateless** conectado ao **Redux**

```javascript
import React from 'react';
import { View, Text } from 'react-native';

import { connect } from 'react-redux';

// import styles from './styles'

const $1 = props => {
  return (
    <View>
      <Text>$1 Component</Text>
    </View>
  );
};

const mapStateToProps = state => ({});

export default connect(mapStateToProps)($1);
```

### `rnc-redux-dispatch` Cria um Componente **Stateless** conectado ao **Redux** que usa **Actions**

```javascript
import React from 'react';
import { View, Text } from 'react-native';

import { connect } from 'react-redux';

// import styles from './styles'

const $1 = props => {
  return (
    <View>
      <Text>$1 Component</Text>
    </View>
  );
};

const mapStateToProps = state => ({});

const mapDispatchToProps = dispatch => ({});

export default connect(
  mapStateToProps,
  mapDispatchToProps
)($1);
```

## React Native Components - Typescript

### `rnc` Cria um Componente **Stateless**

```ts
import React from 'react';
import { View, Text } from 'react-native';

// import styles from './styles'

interface OwnProps {}

type Props = OwnProps;

const $1 = (props: Props) => {
  return (
    <View>
      <Text>$1 Component</Text>
    </View>
  );
};

export default $1;
```

### `rnc-redux` Cria um Componente **Stateless** conectado ao **Redux**

```ts
import React from 'react';
import { View, Text } from 'react-native';

import { connect } from 'react-redux';

// import styles from './styles'

interface StateProps {}

interface OwnProps {}

type Props = StateProps & OwnProps;

const $1 = (props: Props) => {
  return (
    <View>
      <Text>$1 Component</Text>
    </View>
  );
};

const mapStateToProps = state => ({});

export default connect(mapStateToProps)($1);
```

### `rnc-redux-dispatch` Cria um Componente **Stateless** conectado ao **Redux** que usa **Actions**

```ts
import React from 'react';
import { View, Text } from 'react-native';

import { connect } from 'react-redux';

// import styles from './styles'

interface StateProps {}

interface DispatchProps {}

interface OwnProps {}

type Props = StateProps & DispatchProps & OwnProps;

const $1 = (props: Props) => {
  return (
    <View>
      <Text>$1 Component</Text>
    </View>
  );
};

const mapStateToProps = state => ({});

const mapDispatchToProps = dispatch => ({});

export default connect(
  mapStateToProps,
  mapDispatchToProps
)($1);
```
