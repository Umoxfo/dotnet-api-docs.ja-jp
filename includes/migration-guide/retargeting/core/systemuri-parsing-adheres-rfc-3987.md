### <a name="systemuri-parsing-adheres-to-rfc-3987"></a><span data-ttu-id="6ebfd-101">System.Uri 解析が RFC 3987 に準拠</span><span class="sxs-lookup"><span data-stu-id="6ebfd-101">System.Uri parsing adheres to RFC 3987</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6ebfd-102">説明</span><span class="sxs-lookup"><span data-stu-id="6ebfd-102">Details</span></span>|<span data-ttu-id="6ebfd-103">.NET 4.5 では、URI 解析がいくつかの点で変更されました。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-103">URI parsing has changed in several ways in .NET 4.5.</span></span> <span data-ttu-id="6ebfd-104">ただし、これらの変更は .NET 4.5 を対象としたコードのみに影響することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-104">Note, however, that these changes only affect code targeting .NET 4.5.</span></span> <span data-ttu-id="6ebfd-105">バイナリが .NET 4.0 を対象としている場合、以前の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-105">If a binary targets .NET 4.0, the old behavior will be observed.</span></span> <span data-ttu-id="6ebfd-106">.NET 4.5 での URI 解析の変更は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-106">Changes to URI parsing in .NET 4.5 include:</span></span><ul><li><span data-ttu-id="6ebfd-107">URI 解析は、RFC 3987 の最新の IRI 規則に従って、正規化と文字チェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-107">URI parsing will perform normalization and character checking according to the latest IRI rules in RFC 3987.</span></span></li><li><span data-ttu-id="6ebfd-108">Unicode 正規化フォーム C は、URI のホスト部分でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-108">Unicode normalization form C will only be performed on the host portion of the URI.</span></span></li><li><span data-ttu-id="6ebfd-109">無効な mailto: URI は、例外の原因になります。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-109">Invalid mailto: URIs will now cause an exception.</span></span></li><li><span data-ttu-id="6ebfd-110">パス セグメントの最後の末尾のドットが保存されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-110">Trailing dots at the end of a path segment are now preserved.</span></span></li><li><span data-ttu-id="6ebfd-111"><code>file://</code> URI は <code>?</code> 文字をエスケープしません。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-111"><code>file://</code> URIs do not escape the <code>?</code> character.</span></span></li><li><span data-ttu-id="6ebfd-112">Unicode 制御文字の <code>U+0080</code> から <code>U+009F</code> まではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-112">Unicode control characters <code>U+0080</code> through <code>U+009F</code> are not supported.</span></span></li><li><span data-ttu-id="6ebfd-113">コンマ文字 <code>,</code> または <code>%2c</code> は自動的にエスケープ解除されません。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-113">Comma characters <code>,</code> or <code>%2c</code> are not automatically unescaped.</span></span></li></ul>|
|<span data-ttu-id="6ebfd-114">提案される解決策</span><span class="sxs-lookup"><span data-stu-id="6ebfd-114">Suggestion</span></span>|<span data-ttu-id="6ebfd-115">古い .NET 4.0 URI 解析セマンティクスが必要な場合 (めったにありません)、.NET 4.0 を対象とすることによって使用できます。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-115">If the old .NET 4.0 URI parsing semantics are necessary (they often aren't), they can be used by targeting .NET 4.0.</span></span> <span data-ttu-id="6ebfd-116">これは、アセンブリで <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> を使用することによって、または、[プロジェクトのプロパティ] ページの Visual Studio のプロジェクト システム UI によって実現できます。</span><span class="sxs-lookup"><span data-stu-id="6ebfd-116">This can be accomplished by using a <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> on the assembly, or through Visual Studio's project system UI in the 'project properties' page.</span></span>|
|<span data-ttu-id="6ebfd-117">スコープ</span><span class="sxs-lookup"><span data-stu-id="6ebfd-117">Scope</span></span>|<span data-ttu-id="6ebfd-118">Major</span><span class="sxs-lookup"><span data-stu-id="6ebfd-118">Major</span></span>|
|<span data-ttu-id="6ebfd-119">バージョン</span><span class="sxs-lookup"><span data-stu-id="6ebfd-119">Version</span></span>|<span data-ttu-id="6ebfd-120">4.5</span><span class="sxs-lookup"><span data-stu-id="6ebfd-120">4.5</span></span>|
|<span data-ttu-id="6ebfd-121">型</span><span class="sxs-lookup"><span data-stu-id="6ebfd-121">Type</span></span>|<span data-ttu-id="6ebfd-122">再ターゲット中</span><span class="sxs-lookup"><span data-stu-id="6ebfd-122">Retargeting</span></span>|
|<span data-ttu-id="6ebfd-123">影響を受ける API</span><span class="sxs-lookup"><span data-stu-id="6ebfd-123">Affected APIs</span></span>|<ul><li><xref:System.Uri.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.UriKind)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.Uri,System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li></ul>|
