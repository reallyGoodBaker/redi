# redi

![Stars](https://badgen.net/github/stars/wendellhu95/redi)
![Downloads](https://badgen.net/npm/dt/@wendellhu/redi)
![License](https://badgen.net/github/license/wendellhu95/redi)
[![Codecov](https://img.shields.io/codecov/c/github/wendellhu95/redi.svg)](https://codecov.io/gh/wendellhu95/redi)

A dependency library for TypeScript and JavaScript, along with a binding for React.

## Overview

```typescript
import { Inject } from '@wendellhu/redi'

class AuthService {
    public getCurrentUserInfo(): UserInfo {}
}

class FileListService {
    constructor(@Inject(AuthService) private readonly authService: AuthService) {}

    public getUserFiles(): Promise<Files> {
        const currentUser = this.authService.getCurrentUserInfo()
    }
}

const injector = new Injector([[AuthService], [FileListService]])

injector.get(AuthService)
```

**View full documentation on [redi.wendell.fun](https://redi.wendell.fun/).**

## Links

-   [Demo TodoMVC](https://wendellhu95.github.io/redi-todomvc/) | [source](https://github.com/wendellhu95/redi-todomvc)
-   Doc site [source](https://github.com/wendellhu95/redi-site)
-   [scaffold](https://github.com/wendellhu95/redi-starter)

## Users

-   Team Lark at ByteDance

## License

MIT. Copyright 2021-2022 Wendell Hu.
