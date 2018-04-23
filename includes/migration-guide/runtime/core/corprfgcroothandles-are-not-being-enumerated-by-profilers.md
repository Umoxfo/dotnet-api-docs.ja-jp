### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a><span data-ttu-id="4a304-101">COR_PRF_GC_ROOT_HANDLE がプロファイラーで列挙されていない</span><span class="sxs-lookup"><span data-stu-id="4a304-101">COR_PRF_GC_ROOT_HANDLEs are not being enumerated by profilers</span></span>

|   |   |
|---|---|
|<span data-ttu-id="4a304-102">説明</span><span class="sxs-lookup"><span data-stu-id="4a304-102">Details</span></span>|<span data-ttu-id="4a304-103">.NET Framework v4.5.1 では、プロファイル API <code>RootReferences2()</code> が正しく <code>COR_PRF_GC_ROOT_HANDLE</code> を返しません (代わりに、<code>COR_PRF_GC_ROOT_OTHER</code> として返される)。</span><span class="sxs-lookup"><span data-stu-id="4a304-103">In the .NET Framework v4.5.1, the profiling API <code>RootReferences2()</code> is incorrectly never returning <code>COR_PRF_GC_ROOT_HANDLE</code> (they are returned as <code>COR_PRF_GC_ROOT_OTHER</code> instead).</span></span> <span data-ttu-id="4a304-104">この問題は、.NET Framework 4.6 以降で修正されています。</span><span class="sxs-lookup"><span data-stu-id="4a304-104">This issue is fixed beginning in the .NET Framework 4.6.</span></span>|
|<span data-ttu-id="4a304-105">提案される解決策</span><span class="sxs-lookup"><span data-stu-id="4a304-105">Suggestion</span></span>|<span data-ttu-id="4a304-106">この問題は .NET Framework 4.6 で修正されたため、このバージョンの .NET Framework にアップグレードすることによって対処できます。</span><span class="sxs-lookup"><span data-stu-id="4a304-106">This issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="4a304-107">スコープ</span><span class="sxs-lookup"><span data-stu-id="4a304-107">Scope</span></span>|<span data-ttu-id="4a304-108">マイナー</span><span class="sxs-lookup"><span data-stu-id="4a304-108">Minor</span></span>|
|<span data-ttu-id="4a304-109">Version</span><span class="sxs-lookup"><span data-stu-id="4a304-109">Version</span></span>|<span data-ttu-id="4a304-110">4.5.1</span><span class="sxs-lookup"><span data-stu-id="4a304-110">4.5.1</span></span>|
|<span data-ttu-id="4a304-111">型</span><span class="sxs-lookup"><span data-stu-id="4a304-111">Type</span></span>|<span data-ttu-id="4a304-112">ランタイム</span><span class="sxs-lookup"><span data-stu-id="4a304-112">Runtime</span></span>|
