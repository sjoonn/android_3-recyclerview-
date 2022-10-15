# <div align="center">리싸이클러뷰</div>

## <div align="center">👋🏻 처음 화면 👋🏻</div>
### 제목과 가수 사진과 정보가 보인다.
![스크린샷 2022-10-14 오후 9 51 17](https://user-images.githubusercontent.com/102125786/195851339-82b91ff6-d269-41f1-b302-a86ff996d4d3.png)

## <div align="center">📱 사용 방법 📱</div>
### 리싸이클러뷰가 큰틀은 세로로 그안에 가로로 이루어져있다.
![스크린샷 2022-10-14 오후 9 53 00](https://user-images.githubusercontent.com/102125786/195851652-db67e7f8-6dac-42a6-aec8-99c0f217d615.png)
### 가수 사진을 누르면 가수 페이지로 넘어간다.
![스크린샷 2022-10-14 오후 9 54 26](https://user-images.githubusercontent.com/102125786/195851920-1bdfbe4f-78b8-432c-a403-9ae6aab675bc.png)

## <div align="center"> ✍🏻 중요한 내용 ✍🏻 </div>
### singer Data class
```kotlin
  @Parcelize
data class Singer(
	var name: String,
	var info: String,
	var imgUrl: String,
	var discList: List<Disc>
) : Parcelable
```

### disc Data class
```kotlin
  @Parcelize
data class Disc(
	var title: String,
	var info: String,
	var imgUrl: String
) : Parcelable
```
### singer Activity
```kotlin
		val singer = intent.getParcelableExtra<Singer>("singerObj")
		Glide.with(this)
			.load(singer?.imgUrl)
			.into(binding.ivProfile)
		binding.tvName.text = singer?.name
		binding.tvInfo.text = singer?.info
```

## <div align="center"> 😅 미흡한 부분 😅 </div>
### 가수 페이지에 내용이 부족하다...
### Disc Activity에 기능이 없다...
