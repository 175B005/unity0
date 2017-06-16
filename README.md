# unity0
- unityのメモ
- [スクリプト(index)](https://docs.unity3d.com/ja/current/ScriptReference/index.html)
- Unity→オブジェクト指向（単体に機能をつけるためコンポーネント指向とも考えられる。）
- 
```cs
	//マウスが重なった時の処理↓
	void OnMouseEnter(){//
		//ぶつかったら消す
		//destroy(=実体)→そのものを消す

		Debug.Log("hit");
		Destroy (gameObject);
		//gameObject.SetActive(false);動作無効。非表示
		//生成。削除は処理が重い、、、
```
- hierarchy以下のcreate でいろんなオブジェクトが作れる。
- textboxでスコア表示→text内容を変えていく
- スクリプトを使いたいだけの場合は
- 
```cs
public class manager : MonoBehaviour {

	public Text scoreText;
	int iTime = 0;

	void Start () {
		
	}
	
	// Update is called once per frame
	void Update () {
		iTime++;
		scoreText.text = "" + iTime;
```
