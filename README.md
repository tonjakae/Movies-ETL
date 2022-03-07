# Movies-ETL

## Purpose
The purpose of our analysis was to determine whether or not there was positivity bias in relation to 5 star ratings between paid vine reviews and non paid vine reviews. To do so we created a set of paid for vine reviews and non paid for vine reviews, then took the 5 star average of each one respectively the resulting percentages reflected below

### This new assignment consists of two technical analysis deliverables and a written report.

* Deliverable 1: Perform ETL on Amazon Product Reviews
* Deliverable 2: Determine Bias of Vine Reviews
* Deliverable 3: A Written Report on the Analysis README.md

## Deliverable 1 Requirements:
* An ETL function is written to read in the three data files

* The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

* The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

* The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

<img width="523" alt="image" src="https://user-images.githubusercontent.com/87340105/156967382-74f530a3-62e0-4cda-9a10-e72a7cc96a04.png">

<img width="509" alt="image" src="https://user-images.githubusercontent.com/87340105/156967336-be69413f-d07e-4cad-a585-bc46d0337053.png">

<img width="799" alt="image" src="https://user-images.githubusercontent.com/87340105/156967789-680cbf7c-1568-4822-b5cb-9a6074c4f3cf.png">

<img width="818" alt="image" src="https://user-images.githubusercontent.com/87340105/156967804-97eafde6-094f-4e57-b166-bb5566940d63.png">

<img width="250" alt="image" src="https://user-images.githubusercontent.com/87340105/156967830-d8b78fbe-a1ea-4598-ba84-a0f4c06dbdec.png">


## Deliverable 2 Requirements:
* The TV shows are filtered out, and the wiki_movies_df DataFrame is created.

<img width="473" alt="image" src="https://user-images.githubusercontent.com/87340105/156968101-22dcc92f-bca3-4e1b-842a-59ea638e8b9d.png">

* A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.

<img width="658" alt="image" src="https://user-images.githubusercontent.com/87340105/156968205-5516be2f-6149-452e-9af3-728567264759.png">

* The extraction and transformation of the Wikipedia data in the ETL function does the following:
  * A list comprehension is used to keep columns with non-null values.

<img width="644" alt="image" src="https://user-images.githubusercontent.com/87340105/156968558-a1d18fb7-19af-43f3-8f69-377dccd9a462.png">

  * The non-null box office data is converted to string values using the lambda and join functions.

<img width="592" alt="image" src="https://user-images.githubusercontent.com/87340105/156968600-dac0e50e-e2a7-47b9-8892-a03b4d9f36aa.png">

  * A regular expression is used to match the six elements of "form_one" of the box office data.

<img width="545" alt="image" src="https://user-images.githubusercontent.com/87340105/156968627-97e05f47-cfa1-4ac0-b949-a2e3f341b4b2.png">

  * A regular expression is used to match the three elements of "form_two" of the box office data.

<img width="556" alt="image" src="https://user-images.githubusercontent.com/87340105/156968674-990f2459-7616-4389-913b-f400e814460c.png">

<img width="479" alt="image" src="https://user-images.githubusercontent.com/87340105/156968736-cf65d6bc-f0eb-48f1-9fc8-8dd298be3035.png">

  * The following columns are cleaned in the Wikipedia DataFrame:
    * The box office column 
    * The budget column

<img width="643" alt="image" src="https://user-images.githubusercontent.com/87340105/156969161-23893666-655f-4aba-bcc3-c209ce185fa3.png">

    * The release date column
    * The running time column
    
<img width="682" alt="image" src="https://user-images.githubusercontent.com/87340105/156969212-39501dea-224c-40ca-b64f-0f15b876a6e5.png">

 * The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file.

<img width="742" alt="image" src="https://user-images.githubusercontent.com/87340105/156969352-6b51bc24-1bbf-431e-bf66-c0e8e3c38f3d.png">

## Deliverable 3 Requirements

The extraction and transformation of the Kaggle metadata using the ETL function does the following:
* The Kaggle metadata is cleaned.
* The Wikipedia and Kaggle DataFrames are merged.
* The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df:
 * Unnecessary columns are dropped.
 * A function is used to fill in the missing Kaggle data.
 * The movies_df DataFrame is filtered to keep specific columns.
 * The movies_df DataFrame columns are renamed.
The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
* The ratings counts are cleaned.
* The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame.
* The empty values in the movies_with_ratings_df DataFrame are filled with “0”.
The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file.

<img width="481" alt="image" src="https://user-images.githubusercontent.com/87340105/156969786-99cee62b-30ff-47e8-a9ed-712e302cc8a4.png">

<img width="685" alt="image" src="https://user-images.githubusercontent.com/87340105/156969832-e4e99703-b0ce-48e1-8b07-03adbe35f0ef.png">

<img width="416" alt="image" src="https://user-images.githubusercontent.com/87340105/156969860-a7da4471-1c89-4119-b56a-6a66994c7797.png">

<img width="461" alt="image" src="https://user-images.githubusercontent.com/87340105/156969891-3ad4e8c3-0f78-4ad4-b312-a2ea2ac6903d.png">

<img width="730" alt="image" src="https://user-images.githubusercontent.com/87340105/156969933-3eb8956d-3fa3-4fd5-86c7-4cce05a938fc.png">

<img width="641" alt="image" src="https://user-images.githubusercontent.com/87340105/156969962-bf6264ac-ef21-44f7-bc0a-e9991dc00a59.png">

<img width="725" alt="image" src="https://user-images.githubusercontent.com/87340105/156969989-10e9a6f5-69b5-465b-8340-cf23fa9b4f36.png">

<img width="752" alt="image" src="https://user-images.githubusercontent.com/87340105/156970046-54c38e9b-86ec-403a-b5a0-27a7065e18a2.png">

<img width="743" alt="image" src="https://user-images.githubusercontent.com/87340105/156970071-2c6f4978-9098-48e4-88c9-b2b7dc8b168f.png">

<img width="737" alt="image" src="https://user-images.githubusercontent.com/87340105/156970086-86c9200b-7dc4-42ec-ad9f-4060def20565.png">

