# normalize-imports

## Install

```shell
$ stack install
```

## Sort and align Haskell import statements

Given a file

```haskell
import Foo
import qualified Bar

import FooBar
import Baz
```
when you run `:%!normalize-imports` in Vim, you will get

```haskell
import qualified Bar
import           Foo

import           Baz
import           FooBar
```

(better still, map it in your `.vimrc`, e.g. `map <Leader>f :%!normalize-import <CR>`
