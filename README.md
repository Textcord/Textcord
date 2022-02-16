# Textcord
___

### Utility

- Textcord Ansi Maker
> [Textcord-Ansi-Maker](https://ansi.textcord.ga/)
>> [Repository](https://github.com/Textcord/Ansi-Maker)

___

## MarkDown

- *이탤릭*
> ```MarkDown
>> *italics* or _italics_

- **굵게**
> ```MarkDown
>> **bold**

- ***굵은 이탤릭***
> ```MarkDown
>> ***bold italics***

- <ins>밑줄</ins>
> ```MarkDown
>> __underline__

- <ins>*밑줄 이탤릭*</ins>
> ```MarkDown
>> __*underline italics*__

- <ins>**밑줄 굵게**</ins>
> ```MarkDown
>> __**underline bold**__

- <ins>***밑줄 굵은 이탤릭***</ins>
> ```MarkDown
>> __***underline bold italics***__

- ~~정정하기~~
> ```MarkDown
>> ~~Strikethrough~~

___

## ANSI

__**색상이 있는 메시지:**__

Discord는 이제 코드 블록 내에서 컬러 메시지를 보내는 기능을 서서히 출시하고 있습니다. ANSI 색상 코드를 사용하므로 Python 또는 다른 언어로 터미널이나 콘솔에서 색상 텍스트를 인쇄하려고 시도했다면 쉬울 것입니다.

컬러 텍스트를 보낼 수 있으려면 코드 블록에 'ansi' 언어를 사용하고 텍스트를 작성하기 전에 이 형식의 접두사를 제공해야 합니다.
```
\u001b[{format};{color}m
```
*`\u001b`는 ESCAPE/ESC의 유니코드입니다. [](http://www.unicode-symbol.com/u/001B.html) 참조. **봇 없이 직접 사용하려면 웹사이트에서 캐릭터를 복사하여 붙여넣으셔야 합니다.***

이것을 작성한 후 원하는 텍스트를 입력할 수 있으며 색상을 원래대로 되돌리려면 접두사로 `\u001b[0m`을 사용해야 합니다.

다음은 `{format}`을 대체하는 데 사용할 수 있는 값 목록입니다.
* 0: 일반
* 1: **굵게**
* 4: <ins>밑줄</ins>

다음은 `{color}`에 들어갈수 있는 값 목록입니다.
*다음 값은 **텍스트** 색상을 변경합니다.*
* 30: 회색
* 31: 빨간색
* 32: 초록색
* 33: 노란색
* 34: 파란색
* 35: 분홍색
* 36: 청록색
* 37: 하양색

*다음 값은 **텍스트 배경** 색상을 변경합니다.*

* 40: 매우 진한 파란색
* 41: 주황색
* 42: 회색
* 43: 밝은 회색
* 44: 더 밝은 회색
* 45: 남색
* 46: 조금 더 밝은 회색
* 47: 하양색

예를 들어 매우 진한 파란색 배경의 굵은 초록색 텍스트를 원합니다.
나는 단순히 `\u001b[0;40m`(배경색)과 `\u001b[1;32m`(텍스트 색상)을 접두사로 사용합니다. 순서가 **중요합니다**. 먼저 배경색을 지정한 다음 텍스트 색상을 지정합니다.<br>
또는 `\u001b[1;40;32m`과 같은 단일 접두사로 직접 결합할 수도 있고 여러 값을 사용할 수도 있습니다. `\u001b[1;40;4;32m`과 같은 것은 텍스트에 밑줄을 긋고, 굵게 만들고, 초록색으로 만들고, 진한 파란색 배경을 갖습니다.

원본 메시지:<br>
\`\`\`ansi<br>
\u001b[0;40m\u001b[1;32mThat's some cool formatted text right?
or
\u001b[1;40;32mThat's some cool formatted text right?
\`\`\`

결과:<br>
![Background and text color](https://media.discordapp.net/attachments/739937507768270939/930460020603224084/Background-Text-Color.png)

Discord에서 색상이 어떻게 보이는지는 아래 이미지와 같습니다^^

참고: 변경 사항이 아직 귀하나 다른 사용자에게 전달되지 않은 경우 그 동안 다른 코드 블록을 사용하여 컬러 텍스트를 얻을 수 있습니다. 이 gist를 참조하십시오: <https://gist.github.com/matthewzring/9f7bbfd102003963f9be7dbcf7d40e51>

![ANSI Colors](https://media.discordapp.net/attachments/739937507768270939/930825555803263016/ANSI-Colors.png)

[참고(~~사실 번역이긴한ㄷ~~)](https://gist.github.com/kkrypt0nn/a02506f3712ff2d1c8ca7c9e0aed7c06#file-ansi-colors-discord-md)

___
