<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <h1 align="center">Yii 2 Basic Project Template with Bootstrap 4</h1>
    <br>
</p>

This is Yii2 Basic Project template with Bootstrap 4.
Bootstrap 3 is completely removed from project.

INSTALLATION
------------

Checkout [Yii 2 Basic Project Template](https://github.com/yiisoft/yii2-app-basic) for installation instructions.

### Fixing action buttons in GridView
After removing bootstrap 3 and installing bootstrap 4 you will probably see empty
action column in grid view.
Something similar to this.

![Alt](https://i.imgur.com/xVg5Ec5.jpg)

To fix this you need to change the action column class of your GridView into `app\grid\ActionColumn`.

```php
<?= \yii\grid\GridView::widget([
    // ...
    'columns' => [
        // ...
        ['class' => 'app\grid\ActionColumn'],
    ],
]); ?>
```
####In order this to work you need to include font-awesome 5 icons as well.


![Alt](https://i.imgur.com/PNS6PBA.jpg)

------

### Fixing pager of GridView/ListView

By default pager on GridView and ListView looks ugly as well.

![Alt](https://i.imgur.com/4dAgsBu.jpg)

To fix this you need to add pager to GridView or ListView widgets

```php
<?= \yii\grid\GridView::widget([
    'pager' => [
        'class' => \yii\bootstrap4\LinkPager::class
    ],
]);
// For list view
\yii\widgets\ListView::widget([
    'pager' => [
        'class' => \yii\bootstrap4\LinkPager::class
    ],
]);
```

And this is how your pager will look like

![Alt](https://i.imgur.com/WuvzRoj.jpg)


