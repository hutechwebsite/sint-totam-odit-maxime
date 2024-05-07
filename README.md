## k-number

숫자를 입력하면 한글 수사로 반환하는 기능을 제공하는 라이브러리입니다. 예를들면, `10000`을 입력하면 `만`으로 반환합니다.

## Install

```bash
npm install @hutechwebsite/sint-totam-odit-maxime
```

## Usage

```ts
import { kNumber } from '@hutechwebsite/sint-totam-odit-maxime';

const result = kNumber(39_393_382);
console.log('result:', result);
// result: 삼천구백삼십구만삼천삼백팔십이

const unitOnlyResult = kNumber(39_393_382, { format: 'unit-only' });
console.log('unitOnlyResult:', unitOnlyResult);
// unitOnlyResult: 3천9백3십9만3천3백8십2
```

- :warning: 소수점 입력을 지원하지 않습니다. [integer only]
- :warning: 최대값 9_007_199_254_740_991까지만 입력이 가능합니다. 
- :warning: 최소값 -9_007_199_254_740_991까지만 입력이 가능합니다. 

## KNumber

### input
- Number
  - type: number (integer only)
  - example:
    ```ts
    kNumber(123_123)
    ```
- Config
  - type: KNumberConfig
    ```ts
    {
      format?: 'korean-only' | 'unit-only';
    }
    ``` 
  - example: 
    ```ts
    kNumber(123_123, { format: 'unit-only' })
    ```

### output
- type: string
- example:
  ```ts
  const koreanNumber = kNumber(123_123, { format: 'unit-only' });
  console.log(koreanNumber); // 1십2만3천1백2십3
  ```

## Types & Constants
- [type.ts](https://github.com/hutechwebsite/sint-totam-odit-maxime/blob/master/src/types/index.ts)
- [constants.ts](https://github.com/hutechwebsite/sint-totam-odit-maxime/blob/master/src/constants/index.ts)
- [errors.ts](https://github.com/hutechwebsite/sint-totam-odit-maxime/blob/master/src/errors/index.ts)

## License

[MIT](./LICENSE)