---
layout: 'home'
sidebar: false
title: 'The IDE for Minecraft Add-Ons'
description: 'bridge. is a light-weight, yet powerful, IDE for Minecraft add-ons.'

hero:
    name: bridge.
    text: The IDE for Minecraft Add-Ons
    tagline: 軽量、パワフル、使いやすい！
    image:
        src: /favicon.svg
        alt: bridge. logo
    actions:
        - theme: brand
          text: ダウンロード
          link: /guide/download/
        - theme: alt
          text: ブラウザで開く
          link: https://editor.bridge-core.app/

features:
    - icon: ⚡️
      title: 爆速！
      details: 'bridge. を使った開発は、拡張可能なコンパイラアーキテクチャ、充実したオートコンプリート機能、そして作業中の内容をリアルタイムでプレビューできる機能のおかげで、より迅速に行えます。'
      link: /guide/features/
      linkText: 詳細はこちら
    - icon: 🛠️
      title: 拡張性！
      details: 'カスタムコンポーネント、カスタムコマンド、ファイルプリセット、テーマ：bridge.の拡張機能を使えば、ほぼ何でも実現できます。すでに充実した拡張機能のエコシステムから、お好みのものを選ぶことができます。'
      link: /extensions/
      linkText: 詳細はこちら
    - icon: 🚀
      title: シームレス！
      details: 'bridge. はMinecraftとシームレスに連携し、ビヘイビアパック、リソースパック、スキンパック、ワールドを自動的に com.mojang フォルダに同期します。'
      link: /guide/misc/com-mojang-syncing/
      linkText: 詳細はこちら
---

<script setup>
import Creations from "../.vitepress/theme/components/Creations.vue"
import creations from '../data/creations.json'

const creationsJa = [
  {
		"title": "PAC-MAN",
		"image": "/creations\\pac-man\\main.jpg",
		"author": "gamemode-one",
		"excerpt": "伝説のアーケード名作パックマンがマインクラフトに登場！",
		"tags": ["minigame"],
		"download": "https://www.minecraft.net/ja-jp/pdp?id=366e895b-d090-4151-a83a-e86c6b339732"
	},
	{
		"title": "Ultimate Dragons",
		"image": "/creations\\ultimate-dragons\\main.jpg",
		"excerpt": "ドラゴンの背に乗って、破壊的な炎を吹き吐け！驚異的な精度とスピードを極め、ドラゴンの飛行マスターとなれ！",
		"tags": ["dragons", "story", "adventure"],
		"author": "gamemode-one",
		"download": "https://www.minecraft.net/ja-jp/pdp/?id=c1c2dddd-9a10-4013-8adb-adf472560ad2"
	},
	{
		"title": "Planes",
		"image": "/creations\\planes\\main.jpg",
		"excerpt": "パイロットになって、大空を飛び回ろう！",
		"tags": ["flight", "simulation", "steampunk"],
		"author": "cubed-creations",
		"download": "https://www.minecraft.net/ja-jp/pdp?id=7e9fd987-5928-4044-bcce-ca03bde1bce0"
	},
	{
		"title": "Elemental Weapons",
		"image": "/creations\\elemental-weapons\\main.jpg",
		"excerpt": "「エレメンタル・ウェポン」アドオンで、新たな武器をクラフトしよう！",
		"tags": ["weapons", "elemental"],
		"author": "cubed-creations",
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=83532c00-4240-453e-b035-b061479c89f5"
	},
	{
		"title": "HOW TO TRAIN YOUR DRAGON",
		"image": "/creations\\httyd\\main.jpg",
		"excerpt": "ここは、バイキングとドラゴンが暮らす島、バーク！",
		"tags": ["adventure", "dragons"],
		"author": "gamemode-one",
		"download": "https://www.minecraft.net/ja-jp/pdp?id=4f7cf58b-e6d7-46ea-9f8c-206d97f2bafe"
	},
	{
		"title": "Minecraft: Sonic the Hedgehog",
		"image": "/creations\\sonic\\main.jpg",
		"author": "gamemode-one",
		"excerpt": "ソニック・ザ・ヘッジホッグが超音速でマインクラフトに参戦！",
		"tags": ["platformer", "retro", "racing"],
		"download": "https://www.minecraft.net/ja-jp/pdp?id=3086206d-62b3-45ff-a0a8-968b8de33082"
	},
	{
		"title": "Sci-Fi Weapons",
		"image": "/creations\\scifi-weapons\\main.jpg",
		"excerpt": "このSF武器拡張パックで、必要なクラフトレシピを確認し、必要なアイテムをすべて集めて、新しい武器をクラフトしましょう！",
		"tags": ["weapons", "craftable", "sci-fi"],
		"author": "cubed-creations",
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=c5f18417-c1e1-49e6-9218-d18858d1f5c5"
	},
	{
		"title": "The Redstone Temple",
		"image": "/creations\\the-redstone-temple\\main.jpg",
		"excerpt": "あなたの世界は崩壊してしまった。果てしなく広がる砂と太陽の中に迷い込み、残された場所は「レッドストーン神殿」だけだ。",
		"tags": ["rtx", "puzzle"],
		"author": "gamemode-one",
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=773f30e7-0e6d-4751-a15e-173cd9d4f0c4"
	},
	{
		"title": "AVATAR LEGENDS",
		"image": "/creations\\avatar-legends\\main.jpg",
		"featured": true,
		"excerpt": "あなたは、光と平和の化身「アバター」。今、Minecraftの世界に降り立つ！",
		"tags": ["avatar", "rpg", "adventure"],
		"author": "gamemode-one",
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=adf08b99-bba0-4469-99c2-44e1a8239fb9"
	},
	{
		"title": "FurniDeco",
		"image": "/creations\\furnideco\\main.png",
		"excerpt": "FurniDecoには、バニラスタイルにマッチする、機能的で装飾性が高く、ユニークなデザインの家具が25点追加されました。",
		"tags": ["furniture", "decoration"],
		"author": "arexon",
		"download": "https://github.com/arexon/furnideco"
	},
	{
		"title": "Seaside Story",
		"image": "/creations\\seaside-story\\main.jpg",
		"author": "gamemode-one",
		"excerpt": "あなただけの穏やかな海の冒険を満喫しましょう！",
		"tags": ["ocean", "fishing", "relaxing"],
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=5c7cd39e-9903-477b-b013-1b6b6d2bd9ab"
	},
	{
		"title": "Overpowered Wands",
		"image": "/creations\\overpowered-wands\\main.jpg",
		"excerpt": "必要なクラフトレシピを確認し、必要なアイテムをすべて集めて、超強力な杖をクラフトしよう！",
		"tags": ["wands", "craftable", "magic"],
		"author": "cubed-creations",
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=59359292-77d0-4fd1-a802-3f6d855b3174"
	},
	{
		"title": "Bloom",
		"image": "/creations\\bloom\\main.jpg",
		"excerpt": "静かな森へと足を踏み入れ、長い間放置されていた庭園を発見しよう。",
		"tags": ["exploration", "nature", "flower", "relaxing"],
		"author": "gamemode-one",
		"download": "https://www.minecraft.net/ja-jp/pdp?id=d8604c56-d709-40e1-a286-13dce3b34ac5"
	},
	{
		"title": "Spellrune",
		"image": "/creations\\spellrune\\main.jpg",
		"author": "gamemode-one",
		"excerpt": "Bedrock版のまったく新しいScripting APIが登場！ルーンを組み合わせて、強力な属性魔法をクラフトしよう！",
		"tags": ["magic", "spells", "adventure"],
		"download": "https://www.minecraft.net/marketplace/pdp?id=f5cc05fc-616a-4963-a02b-5db3fcc9e311"
	},
	{
		"title": "DragonFire",
		"image": "/creations\\dragon-fire\\main.png",
		"author": "spectral-studios",
		"excerpt": "ドラゴンの調教師の達人になろう！",
		"developer": "OutLandishly Crafted",
		"tags": ["adventure", "dragons"],
		"download": "https://www.minecraft.net/ja-jp/pdp?id=d8a14066-38ad-4633-bab8-f50ab1817f1c"
	},
	{
		"title": "Advanced Mining",
		"image": "/creations\\advanced-mining\\main.jpg",
		"excerpt": "最高にカッコいい新機械で、思う存分採掘を楽しもう！",
		"tags": ["economy", "mining", "advanced"],
		"author": "gamemode-one",
		"download": "https://www.minecraft.net/ja-jp/pdp?id=56952d12-3c9c-4597-886d-b62f77202e27"
	},
	{
		"title": "DragonFire 2: Nations",
		"image": "/creations\\dragon-fire-2\\main.jpg",
		"author": "spectral-studios",
		"excerpt": "DragonFireシリーズの最新作が登場！",
		"tags": ["adventure", "dragons"],
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=d3eb0ce8-6190-483d-9208-356dc209c173"
	},
	{
		"title": "Voidlands Dimensions",
		"image": "/creations\\voidlands-dimensions\\main.jpg",
		"author": "gamemode-one",
		"excerpt": "他に類を見ないスカイブロック。",
		"tags": ["skyblock", "hardcore", "survival"],
		"download": "https://www.minecraft.net/ja-jp/marketplace/pdp?id=010314fa-71d2-4160-a42b-491fb8a95002"
	},
	{
		"title": "World Against",
		"image": "/creations\\world-against\\main.jpg",
		"author": "xxpoggyislitxx",
		"excerpt": "The Endの中で、あなたは恐ろしい行いを犯したため、別の世界へと追放されてしまいました。その世界では、あらゆるものがあなたを殺そうとしているだけでなく、宇宙そのものもあなたを殺そうとしているのです。",
		"tags": ["bridge-jam", "world-is-your-enemy"],
		"download": "https://discord.com/channels/602097536404160523/961112716863504465/985931887484751872"
	},
	{
		"title": "Frost Fight",
		"image": "/creations\\frost-fight\\main.png",
		"author": "mrdinger",
		"excerpt": "厳しい制限が課されたこの冬の荒野で、あなたはどれだけ長く生き残れるだろうか！ あなたを狙う雪だるまの大群を食い止めるため、防御施設を建設し、アイテムを作り、資源を採掘しよう！",
		"tags": ["bridge-jam", "winter-wonderland"],
		"download": "https://www.mediafire.com/file/026hcotwdvbyyqy/Frost_Fight.zip/file"
	},
	{
		"title": "The World Is Quite Literally Your Enemy",
		"image": "/creations\\world-is-quite-literally-your-enemy\\main.jpg",
		"author": "mcjiprock",
		"excerpt": "このアドオンは、あなたのワールドをかなり生き生きとしたものにする一方で、あなた自身の生存率はかなり低下させてしまいます。",
		"tags": ["bridge-jam", "world-is-your-enemy"],
		"download": "https://discord.com/channels/602097536404160523/961112716863504465/985936185224482907"
	},
	{
		"title": "Snowdown",
		"image": "/creations\\snowdown\\main.png",
		"author": "dingsel",
		"excerpt": "「スノーダウン」はPVEゲームモードで、雪に埋もれた町のタイルを掘り起こすために、家を守りながら次々と押し寄せる敵と戦わなければなりません。",
		"tags": ["bridge-jam", "winter-wonderland"],
		"download": "https://github.com/Dingsel/Snowdown/releases/tag/1.1"
	},
	{
		"title": "Frigid Elysium",
		"image": "/creations\\frigid-elysium\\main.png",
		"author": "braden",
		"excerpt": "「ブライト・ビースト」を倒し、この永遠の冬を終わらせることができるか？　それとも、先にあなたがその冬に飲み込まれてしまうのか？",
		"tags": ["bridge-jam", "winter-wonderland"],
		"download": "https://www.mediafire.com/file/52bp0xxy2ve8bf2/Winter_Wonderland.mcaddon/file"
	},
	{
		"title": "The Corruption",
		"image": "/creations\\the-corruption\\main.png",
		"author": "drp",
		"excerpt": "腐敗が蔓延している……世界が敵となるこのユニークなサバイバルチャレンジで、あなたは生き残れるか？",
		"tags": ["bridge-jam", "world-is-your-enemy"],
		"download": "https://discord.com/channels/602097536404160523/961112716863504465/985927721035112458"
	},
	{
		"title": "High and Dry",
		"image": "/creations\\high-and-dry\\main.png",
		"author": "kekecreations",
		"excerpt": "あなたは不毛の惑星に不時着し、自分が誰なのか、過去の人生について何も覚えていません。さあ、この過酷な新しい世界で、どんな自分になりたいかを決める時が来ました！",
		"tags": ["bridge-jam", "world-is-your-enemy"],
		"download": "https://discord.com/channels/602097536404160523/961112716863504465/985799216792231997"
	},
	{
		"title": "Blood Rot",
		"image": "/creations\\blood-rot\\main.png",
		"author": "braden",
		"excerpt": "あなたの世界を蝕んでいく、嫌悪感を催す新たなバイオーム「ブラッド・ロット」を世界に広めよう。",
		"tags": ["bridge-jam", "world-is-your-enemy"],
		"download": "https://discord.com/channels/602097536404160523/961112716863504465/985780948832485417"
	}
]

const topThreeCreations = creationsJa.filter(creation => creation.featured)
const notFeatured = creationsJa.filter(creation => !creation.featured)
while(topThreeCreations.length < 4) {
  topThreeCreations.push(notFeatured.shift())
}
if(topThreeCreations.length > 3) {
  topThreeCreations.splice(3)
}

</script>

<Creations 
  :items="topThreeCreations" 
  title="インスピレーションを得る" 
  description="bridge. は、最も高度なマインクラフトアドオンのいくつかを強力にサポートしています。私たちのお気に入りの作品をいくつかご紹介します..." 
/>