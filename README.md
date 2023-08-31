# Katakunci-NavMesh
Rangkuman katakunci dari package NavMesh unity

# NavMeshAgent

Ini adalah komponen yang Anda tambahkan ke GameObject untuk mengendalikannya melalui NavMesh.


destination: Tempat tujuan agent.

isStopped: Mengontrol apakah agent berhenti atau bergerak.

speed: Kecepatan agent.

angularSpeed: Kecepatan rotasi agent.

acceleration: Akselerasi agent.

radius: Radius kolider agent.

height: Tinggi kolider agent.

Warp(Vector3 position): Memindahkan agent ke posisi tertentu.

ResetPath(): Menghapus path yang sedang diikuti oleh agent.

SetPath(NavMeshPath path): Menetapkan path yang harus diikuti agent.

Resume(): Melanjutkan pergerakan setelah berhenti.

Stop(): Menghentikan pergerakan agent.

CalculatePath(Vector3 targetPosition, NavMeshPath path): Menghitung path ke target tetapi tidak memulai pergerakan.

# NavMesh

Kelas statis ini digunakan untuk melakukan operasi umum di NavMesh.

CalculatePath(Vector3 sourcePosition, Vector3 targetPosition, int areaMask, NavMeshPath path): Menghitung path antara dua titik.

SamplePosition(Vector3 sourcePosition, out NavMeshHit hit, float maxDistance, int areaMask): Menemukan titik terdekat yang dapat diakses dalam NavMesh dari posisi yang diberikan.

Raycast(Vector3 sourcePosition, Vector3 targetPosition, out NavMeshHit hit, int areaMask): Mengecek apakah ada penghalang di antara dua titik.

FindClosestEdge(Vector3 sourcePosition, out NavMeshHit hit, int areaMask): Menemukan tepi NavMesh terdekat dari posisi yang diberikan.

CalculateTriangulation(): Mengembalikan data triangulasi dari seluruh NavMesh.

# NavMeshPath

Mengandung informasi tentang sebuah path di NavMesh.

corners: Titik-titik yang menggambarkan jalur dari awal ke tujuan.

status: Status dari path (Invalid, Complete, Partial).

# NavMeshObstacle

Menggunakan kolider untuk menentukan area yang harus dihindari oleh NavMeshAgent.

carving: Memutuskan apakah obyek ini mempengaruhi NavMesh pada runtime.

size: Ukuran obyek.

center: Posisi tengah dari obyek.

# NavMeshHit

Digunakan untuk menyimpan hasil dari operasi NavMesh seperti Raycast atau SamplePosition.

position: Posisi dari hit.

normal: Normal dari permukaan di titik hit.

distance: Jarak dari awal ray sampai hit.

mask: Area mask dari hit.

# NavMeshLink

Menghubungkan dua area NavMesh yang terpisah, bisa digunakan untuk membuat jembatan atau tangga.

startPoint: Titik awal dari link.

endPoint: Titik akhir dari link.

width: Lebar dari link.

# NavMeshSurface

Komponen ini digunakan untuk membangun NavMesh di scene Anda, memungkinkan Anda untuk melakukan baking NavMesh pada runtime.

BuildNavMesh(): Fungsi ini memulai proses baking.
