IR READ ME 
P-21: Music Subtitles search engine
project description:
	users will have pieces of song lyrics in mind. so, when they want to get the lyrics of the song they have in mind. they should search.
	we are solving the problem using our retrieval model.
	user will give his a query(broken lyrics) , we will show them list of lyrics similar to that.
Group members:
	K. Varuna krishna
	G. Vikram
	K. Venkatesh
	G. Adarsh Kumar
How to run:
download:
	the `documents`,
	the `tfidfValues.pkl`
	the `idfValues.pkl`
	the `ir project.ipynb`
	THE DATASET.XLSX,
keep all these in same folder
change all the paths to necessary paths in `ir project.ipynb` file.
now , run the cells in `ir project.ipynb` file.

Documents Link : https://drive.google.com/drive/folders/1HMlWHjkOeXrT02tq5_YFyB-ch5o1ePzq?usp=sharing
tfidf Link :https://drive.google.com/file/d/1SIfjaUJP2N75aJNCJJHm1uH4Lyl_9Pcs/view?usp=sharing
idf link : https://drive.google.com/file/d/1-7BZDhQsP6yh2OyeOl2IA9fvztjzi-_j/view?usp=sharing
dataset link : https://drive.google.com/file/d/1-68cY9nGS6EqVQnxzfDmJ3W3F3Uoq2QA/view?usp=sharing


cells description :
Indexing and finding tf-idf cell and query processing: 
	If only you dont have the docs and the `tfidfValues.pkl`,`idfValues.pkl` run this cell. this cell finds the tf idf for every document and stores it.
ranking and evaluation cell:
	this cell takes a query and find the tfidf vector and find the top 10 docs similar to it and shows them as result.
	in evaluation part , the retrieved docs will be marked as relevant or non relevant ( human annotation) and will calculate the precision@k and recall@k , for k=1...10
1'st Non trivial task:
	in this we are creating an inverted index (from genre -> docs in that genre)
	Now ,after that when a query comes , we are finding tf-idf vector and 
	retrieving the docs from whole collection. then we take the genre of top document and
	we take all the documents in that genre and do the ranking.
	after this the docs will be retieved and we do evaluation.
2'nd Non Trivial task:
	Creating inverted index : here we create an inverted index:( keyword --> words related to keyword) like : sadness -> cry, lonely,etc..
	here query will be only keywords
	based on the keywords we will get all it's related words from the inverted index and pick 10 words randomly and make it as a query.
	this query will be passed and gets a tf-idf vector and finds the top 10 similar documents from whole collection and 
	sends them as result. then we evaluate this.
	