# 課題 11-1: カプセル化

### 課題の説明
「アクセス修飾の定石」に従って以下のHeroクラスの２つのフィールドをカプセル化し、実行結果が実行例と同じになるようにProgB1.mainメソッドを修正しなさい。
(注意)この課題では、Heroクラスのカプセル化に伴い、ProgB1.main()からのアクセスが正しく変更されないと全てのテストでコンパイルエラーとなる

### Heroクラス（カプセル化する）
```java
public class Hero
{
    String name = "??";
    int hp = 0;

    public void run()
    {
        System.out.println(this.name + "は逃げ出した！");
    }
}
```

### ProgB1クラス（Heroクラスのカプセル化後も同様の結果が得られるように変更する）
```java
public class ProgB1 {

    public static void main(String[] args) {
        Hero h = new Hero();
        h.name = "太郎";
        h.hp = 100;

        System.out.println("勇者" + h.name + " (HP:" + h.hp + ") が誕生した！");
    }

}
```

### 実行例
```
勇者太郎 (HP:100) が誕生した！
```
