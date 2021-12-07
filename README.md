English | [Chinese](./README.CN.md)

# Wia's Components

Components for [wia](https://www.wia.pub) applications.

See [wia components](https://www.wia.pub/doc/component.html) documentation for detailed description.

## install

You will need Node.js installed on your system.

First, install

```bash
$ npm install @wiajs/component
```

## To use

Take uploader as an example, to make a register page

in register.js file:

```js

import Uploader from '@wiajs/component/uploader';

function init(pg)
  _uploader = new Uploader({
    upload: true, // �Զ��ϴ�
    url: _url, // �ϴ���ַ
    dir: 'star/etrip/demo', // ͼƬ�洢·������ʽ: ������/Ӧ������/����
    el: pg.clas('uploader'), // �������
    input: pg.name('avatar'), // �ϴ��ɹ����url��������򣬱����ύ
    choose: pg.name('choose'), // �������ѡ���ļ�

    multiple: false, // �ɷ�ͬʱѡ�����ļ�
    limit: 1, // �ļ������� -1 0 ���ޣ�1 �����Ƶ����ļ����� ͷ��
    accept: 'image/jpg,image/jpeg,image/png,image/gif', // ѡ���ļ�����
    compress: true, // �Զ�ѹ��
    quality: 0.5, // ѹ����

    // xhr����
    data: {}, // ��ӵ�����ͷ������
  });

```

in your register.less file:

```less
@import '@wiajs/component/uploader/index.less';
```

in your register.html file:

```html
  <div class="page-content">
    <form name="fmData">
      <div class="list inline-labels">
        <ul>
          <li class="avatar">
            <a href="" class="item-link item-content">
              <div class="item-title item-label">ͷ��<span>*</span></div>
              <div name="choose" class="item-inner">
                <div class="item-after uploader">
                  <input name="avatar" type="hidden" />
                </div>
              </div>
            </a>
          </li>
        </ul>
      <div>
    </form>
  </div>
```
