# Swagger v2

## Type

https://swagger.io/docs/specification/data-models/data-types/

```yaml
# Integer
timeout:
  type: integer
  description: タイムアウト（秒単位）
  minimum: 1
  maximum: 30
  default: 30

# enum
thumbnail_type:
   type: string
   description: 3値のどれかを設定(small, medium, large)
   enum:
     - small
     - medium
     - large
```

## Tips

* 細かくファイルを分割してもOK
  * definitionのモデルとAPI設計を分けるなど
    * WebのSwagger Editorで確認しにくくなるデメリットが有る
  * go-swaggerなどで結合できるため
* go-swaggerでの自動生成を見越した設計のコツ
  * `Tag` で自動生成したパッケージが決まるため、短い命名にすべき
  * 複数のTagにするとそれぞれで生成される
  * Model設計
    * objectでなくてもrefで参照できる
    * ドメインモデルではないが、なるべくすべての型を切り出したほうが良さげ
      * 例えば、min~max, default value, descriptionなどの設計を統一できる

  

