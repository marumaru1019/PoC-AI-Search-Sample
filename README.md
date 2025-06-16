# AI Search アップデート情報 サンプルリポジトリ

このリポジトリは、Azure AI Search の最新機能をJupyter Notebookで試すことができるサンプル集です。

## 📂 フォルダ構成

### 🤖 agentic-search
**エージェンティック検索のサンプル**
- ファイル: `quickstart-agentic-retrieval.ipynb`
- Azure AI SearchとAzure OpenAIを組み合わせたインテリジェントな検索機能
- [📖 詳細ドキュメント](https://learn.microsoft.com/ja-jp/azure/search/search-agentic-retrieval-concept)

### 🔒 Quickstart-Document-Permissions-Pull-API
**PULL型ドキュメント権限管理のサンプル**
- ファイル: `document-permissions-pull-api.ipynb`
- ユーザーがアクセス時にリアルタイムで権限をチェックする方式
- [📖 詳細ドキュメント](https://learn.microsoft.com/ja-jp/azure/search/search-document-level-access-overview)

### 🚀 Quickstart-Document-Permissions-Push-API
**PUSH型ドキュメント権限管理のサンプル**
- ファイル: `document-permissions-push-api.ipynb`
- 事前にドキュメントに権限情報を付与しておく方式
- [📖 詳細ドキュメント](https://learn.microsoft.com/ja-jp/azure/search/search-document-level-access-overview)

## 🛠️ 環境要件

### 前提条件
- **Python**: 3.11以上
- **Azure リソース**:
  - Azure AI Search サービス
  - Azure OpenAI サービス

## 🚀 環境構築

### 1. リポジトリのクローン
```bash
git clone <repository-url>
cd ai-sample
```

### 2. Python仮想環境の作成・有効化
```bash
# 仮想環境の作成
python -m venv .venv

# 仮想環境の有効化 (Windows)
.venv\Scripts\activate

# 仮想環境の有効化 (macOS/Linux)
source .venv/bin/activate
```

### 3. 各フォルダでの依存関係インストール

各機能を試したいフォルダに移動して、必要なパッケージをインストールしてください：

```bash
# エージェンティック検索を試す場合
cd agentic-search
pip install -r requirements.txt

# PULL型権限管理を試す場合
cd Quickstart-Document-Permissions-Pull-API
pip install -r requirements.txt

# PUSH型権限管理を試す場合
cd Quickstart-Document-Permissions-Push-API
pip install -r requirements.txt
```

### 4. 環境変数の設定

各フォルダ内の`.env`ファイル（または`sample.env`）を参考に、以下の環境変数を設定してください：

```env
# Azure AI Search
AZURE_SEARCH_SERVICE_ENDPOINT=https://your-search-service.search.windows.net
AZURE_SEARCH_INDEX_NAME=your-index-name
AZURE_SEARCH_API_KEY=your-search-api-key

# Azure OpenAI
AZURE_OPENAI_ENDPOINT=https://your-openai-service.openai.azure.com
AZURE_OPENAI_API_KEY=your-openai-api-key
AZURE_OPENAI_API_VERSION=2024-02-01
AZURE_OPENAI_DEPLOYMENT_NAME=your-deployment-name
```

## 📝 使用方法

### Jupyter Notebookの起動
各フォルダで以下のコマンドを実行してJupyter Notebookを起動します：

```bash
jupyter notebook
```

### 各機能の試し方

#### 🤖 エージェンティック検索
1. `agentic-search`フォルダに移動
2. `quickstart-agentic-retrieval.ipynb`を開く
3. セルを順番に実行して機能を体験

#### 🔒 PULL型ドキュメント権限管理
1. `Quickstart-Document-Permissions-Pull-API`フォルダに移動
2. `document-permissions-pull-api.ipynb`を開く
3. セルを順番に実行してPULL型権限制御を体験

#### 🚀 PUSH型ドキュメント権限管理
1. `Quickstart-Document-Permissions-Push-API`フォルダに移動
2. `document-permissions-push-api.ipynb`を開く
3. セルを順番に実行してPUSH型権限制御を体験

## 💡 参考リンク

- [Azure AI Search 公式ドキュメント](https://learn.microsoft.com/ja-jp/azure/search/)
- [Azure OpenAI Service 公式ドキュメント](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/)
