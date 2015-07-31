Jsoneditor Extension for Yii 2
==============================

This extension provides the [Jsoneditor](http://jsoneditoronline.org/) integration for the Yii2 framework.
This package is fork from [DevGroup-ru/yii2-jsoneditor] (https://github.com/DevGroup-ru/yii2-jsoneditor) with active form support, because my pull-request is not merged.


Installation
------------

This extension requires [Jsoneditor](https://github.com/josdejong/jsoneditor/)

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist loveorigami/yii2-jsoneditor "*"
```

or add

```
"loveorigami/yii2-jsoneditor": "*"
```

to the require section of your composer.json.


General Usage
-------------

```php
use lo\widgets\Jsoneditor;

Jsoneditor::widget(
    [
        'editorOptions' => [
            'modes' => ['code', 'form', 'text', 'tree', 'view'], // available modes
            'mode' => 'tree', // current mode
        ],
        'name' => 'editor', // input name. Either 'name', or 'model' and 'attribute' properties must be specified.
        'options' => [], // html options
    ]
)
```
or with active form as

```php
    <?= $form->field($model,'name')->widget(Jsoneditor::className(),
        [
            'editorOptions' => [
				'modes' => ['code', 'form', 'text', 'tree', 'view'], // available modes
				'mode' => 'tree', // current mode
            ],
        ]
    ); ?>
```
