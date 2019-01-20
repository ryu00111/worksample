### lambda

lambdaとは、無名関数（＝名前が付いていない関数）を表現する記法の一つです。

例としてpython言語で、a,bを引数として受け取り、その和を返す関数を記述します。

	def fnuc(a,b):
	    return a+b

この場合、関数にはfuncと命名されています。

これに対し、lambda式を使って、a,dを引数として受け取りその和を返す無名関数を記述すると・・・

	lambda a,b : a+b

となります。

最初の「lambda」は予約語で「これからlambda式で無名関数を定義する」という事を表しています。
defに似ていますが、defが名前付きの関数を定義するのに対し、lambdaは無名の関数を定義します。

lambdaの隣にある a,b は引数を表し、`def func(a,b):`のカッコの中と同じ意味を持っています。  
ちなみに、引数はカンマで区切れば複数使えますし、引数が無くても構いません。

コロンを挟んで右側の a+b が返り値を表し、`return a+b`と同じ意味です。  
戻り値は必ず書かなくてはいけません。


### lambdaを使うメリット

lambdaを使うメリットは、コードを簡潔に書けることが挙げられます。

例として様々な商品の価格を抜き出したリストがあり、そのリストからある金額以上のものを抜き出し、
価格の安い順に並べた情報を取得するプログラムを実装するとします。

lambda式を用いない場合の実装方法の例

	prices = [3000,2500,10500,4300]
	paymentList = []
	for price in prices:
	    if price > 3500:
	        paymentList.append(price)
	
	paymentList.sort()
	
	print(paymentList)
 
実行結果

	[4300, 10500]

これをlambda式を用いて書くと以下のようになります。

	prices = [3000,2500,10500,4300]
	priceList = list(filter(lambda price:price > 3500, prices))
	priceList.sort()
	
	print(priceList)
 
実行結果

	[4300, 10500]

上記サンプルにてlambda式と合わせてlist関数とfilter関数を使用しました。
list関数は引数の値をlist型へ変換し、その後、sort()関数にて並び替えを行うために使用しています。
そして、filter関数は第二引数に指定された配列の各要素に対して、第一引数の関数処理を実施し、
Trueとなるものだけを抽出する処理を行っています。

