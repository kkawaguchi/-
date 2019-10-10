# Java の課題 (初級編)

**注意 (Windows ユーザー): 各ファイルで日本語を使用する場合は Shift JIS で保存するかコンパイル時に ```-encoding UTF-8``` のオプションを指定する**

1. 事前準備を参考に Java の環境を構築する

## 練習問題

1. コンソールに「Hello, World」を表示する
1. コンソールに「Hello, World」を 5 回繰り返して表示する
1. コンソールから文字列を読み取ってそれを表示する
1. コンソールから文字列を読み取って、読み取った文字列を数字に変換し、その回数繰り返してコンソールに「Hello, World」を表示する
1. 1 から 100 までコンソールに表示する。ただし、3 の倍数は Fizz を表示する
1. 1 から 100 までコンソールに表示する。ただし、5 の倍数は Buzz を表示する
1. 1 から 100 までコンソールに表示する。ただし、3 の倍数は Fizz、5 の倍数は Buzz、3 と 5 の倍数は FizzBuzz を表示する

## 課題: カレンダーを出力するプログラムを作成する

1. 曜日のヘッダーと 1 ～ 31 までの数字を 7 列ずつ出力する

```
日 月 火 水 木 金 土
 1  2  3  4  5  6  7
 8  9 10 11 12 13 14
15 16 17 18 19 20 21
22 23 24 25 26 27 28
29 30 31
```

2. カレンダーの出力処理をメソッド化する

```java
public class Calendar {
    public static void main(String[] args) {
        // カレンダーを表示する
        printCalendar();
    }

    private static void printCalendar() {
        // カレンダーの出力処理
    }
}
```

3. カレンダーの出力処理に引数を渡して最初の曜日を指定できるようにする (日曜日を 0、土曜日を 6 とする)

```java
public class Calendar {
    public static void main(String[] args) {
        // 水曜日始まりのカレンダーを表示する
        printCalendar(3);
    }

    private static void printCalendar(int firstDayOfWeek) {
        // カレンダーの出力処理
    }
}
```

出力の例

```
日 月 火 水 木 金 土
          1  2  3  4
 5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28 29 30 31
```

4. カレンダーの出力処理に引数を追加して渡して最初の曜日と月の日数を指定できるようにする

```java
public class Calendar {
    public static void main(String[] args) {
        // 水曜日始まりで28日までのカレンダーを表示する
        printCalendar(3, 28);
    }

    private static void printCalendar(int firstDayOfWeek, int numberOfDaysInMonth) {
        // カレンダーの出力処理
    }
}
```

出力の例

```
日 月 火 水 木 金 土
          1  2  3  4
 5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28
```

5. システム日付のカレンダーを表示する

```java
// システム日付のカレンダーオブジェクトを取得する
Calendar cal = Calendar.getInstance();
// Calendar オブジェクトの日付をシステム日付の 1 日にセットする
cal.set(Calendar.DAY_OF_MONTH, 1);
// 曜日を取得する (0が日曜日)
int firstDayOfWeek = cal.get(Calendar.DAY_OF_WEEK);
// 当月の最終日を取得する
int numberOfDaysInMonth = cal.getActualMaximum(Calendar.DAY_OF_MONTH);
```

## Java アプリケーションの実行方法

1. .java ファイルをコンパイルする

```cmd
C:\excercise-java\101_beginner\Excercises>javac Excercise1.java
```

コンパイルすることで .java ファイルのあるフォルダに .class ファイルが作成されます

2. .class ファイルを実行する

```cmd
C:\excercise-java\101_beginner\Excercises>java Excercise1
```

3. 実行結果

```cmd
Hello, World!
```

## 事前準備

1. JDK8 をインストール
1. [Oracle のサイト](http://www.oracle.com/technetwork/java/javase/downloads/index.html)より、JDKをダウンロードする
1. ダウンロードしたファイルをインストールする
1. インストールが完了したら環境変数に JAVA_HOME を追加する

**環境変数の追加について**

環境変数について知りたい場合は以下のサイトを参考にすること

- [環境変数 - Wikipedia](https://ja.wikipedia.org/wiki/%E7%92%B0%E5%A2%83%E5%A4%89%E6%95%B0)
- [Windows で環境変数 PATH をいじる方法のまとめ](https://qiita.com/sta/items/6d29da0dc7069ffaae60)

