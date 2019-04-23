## Sobre o Projeto

Este projeto visa a disponibilização de um conjunto de Snippets ou atalhos para criação de componentes e arquivos de configuração em aplicações React Native visando a utilização de React Hooks, logo, apenas Stateless Components são criados.

## Começando

![Create React Native Component](https://raw.githubusercontent.com/Rocketseat/rocketseat-vscode-react-native-snippets/master/images/component.gif)

## Linguagens suportadas (extensões de arquivo)

- JavaScript (.js)
- React Native (.js)
- Typescript React Native (.tsx)

## Snippets

Abaixo segue a lista com todos os Snippets disponíveis e os gatilhos para cada um. O **⇥** significa a tecla `TAB`.

## React-hooks

|           Gatilho | Conteúdo                           |
| ----------------: | ---------------------------------- |
|    `state-hook →` | `const [$1, set$1] = useState($2)` |
|      `cdm-hook →` | `useEffect(() => {$0}, []);`       |
| `cdupdate-hook →` | `useEffect(() => {$0});`           |
| `cwumount-hook →` | `useEffect(() => () => {$0}, []);` |

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

const UserRow = props => {
  return (
    <View>
      <Text>UserRow Component</Text>
    </View>
  );
};

const mapStateToProps = state => ({});

const mapDispatchToProps = dispatch => ({});

export default connect(
  mapStateToProps,
  mapDispatchToProps
)(UserRow);
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

const UserRow = (props: Props) => {
  return (
    <View>
      <Text>UserRow Component</Text>
    </View>
  );
};

const mapStateToProps = state => ({});

const mapDispatchToProps = dispatch => ({});

export default connect(
  mapStateToProps,
  mapDispatchToProps
)(UserRow);
```
