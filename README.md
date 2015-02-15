This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more external
libraries included.

Static **ffmpeg v2.5.4** build from this repository currently compiles on:
<table>
<tr><td><b>CentOS 6.6</b>      </td><td>i386 and x86_64</td>
<td rowspan="3">
<img src="http://www.movieconverter-studio.com/_PUBLIC/ffmpeg/logo-new/ffmpeg-logo-src/ffmpeg-logo.png" height="90">
</td></tr>
<tr><td><b>Ubuntu 14.04.1 LTS</b></td><td>i386 and x86_64</td></tr>
<tr><td><b>Debian 7.8</b>      </td><td>i386 and x86_64</td></tr>
</table>

For build see [BUILD.md].

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            2.5.4
C compiler                gcc
C library                 glibc
runtime cpu detection     yes
yasm                      yes
MMX enabled               yes
MMXEXT enabled            yes
3DNow! enabled            yes
3DNow! extended enabled   yes
SSE enabled               yes
SSSE3 enabled             yes
AVX enabled               yes
XOP enabled               yes
FMA3 enabled              yes
FMA4 enabled              yes
i686 features enabled     yes
CMOV is fast              no
EBX available             yes
EBP available             yes
debug symbols             no
strip symbols             yes
optimize for size         no
optimizations             yes
static                    yes
shared                    no
postprocessing support    yes
new filter support        yes
network support           yes
threading support         pthreads
safe bitstream reader     yes
SDL support               no
opencl enabled            no
texi2html enabled         yes
perl enabled              yes
pod2man enabled           yes
makeinfo enabled          yes
makeinfo supports HTML    no

External libraries:
bzlib                   libiec61883             libv4l2
frei0r                  libilbc                 libvidstab
iconv                   libmodplug              libvo_amrwbenc
libaacplus              libmp3lame              libvorbis
libass                  libnut                  libvpx
libbluray               libopencore_amrnb       libwavpack
libbs2b                 libopencore_amrwb       libwebp
libcaca                 libopenjpeg             libx264
libcdio                 libopus                 libx265
libdc1394               librtmp                 libxavs
libfaac                 libschroedinger         libxvid
libfdk_aac              libshine                libzmq
libflite                libsoxr                 libzvbi
libfontconfig           libspeex                lzma
libfreetype             libtheora               zlib
libgsm                  libtwolame

Enabled decoders:
aac                     bfi                     gsm
aac_latm                bink                    gsm_ms
aasc                    binkaudio_dct           h261
ac3                     binkaudio_rdft          h263
ac3_fixed               bintext                 h263i
adpcm_4xm               bmp                     h263p
adpcm_adx               bmv_audio               h264
adpcm_afc               bmv_video               hevc
adpcm_ct                brender_pix             hnm4_video
adpcm_dtk               c93                     huffyuv
adpcm_ea                cavs                    iac
adpcm_ea_maxis_xa       cdgraphics              idcin
adpcm_ea_r1             cdxl                    idf
adpcm_ea_r2             cinepak                 iff_byterun1
adpcm_ea_r3             cljr                    iff_ilbm
adpcm_ea_xas            cllc                    imc
adpcm_g722              comfortnoise            indeo2
adpcm_g726              cook                    indeo3
adpcm_g726le            cpia                    indeo4
adpcm_ima_amv           cscd                    indeo5
adpcm_ima_apc           cyuv                    interplay_dpcm
adpcm_ima_dk3           dca                     interplay_video
adpcm_ima_dk4           dfa                     jacosub
adpcm_ima_ea_eacs       dirac                   jpeg2000
adpcm_ima_ea_sead       dnxhd                   jpegls
adpcm_ima_iss           dpx                     jv
adpcm_ima_oki           dsd_lsbf                kgv1
adpcm_ima_qt            dsd_lsbf_planar         kmvc
adpcm_ima_rad           dsd_msbf                lagarith
adpcm_ima_smjpeg        dsd_msbf_planar         libfdk_aac
adpcm_ima_wav           dsicinaudio             libgsm
adpcm_ima_ws            dsicinvideo             libgsm_ms
adpcm_ms                dvbsub                  libilbc
adpcm_sbpro_2           dvdsub                  libopencore_amrnb
adpcm_sbpro_3           dvvideo                 libopencore_amrwb
adpcm_sbpro_4           dxa                     libopenjpeg
adpcm_swf               dxtory                  libopus
adpcm_thp               eac3                    libschroedinger
adpcm_vima              eacmv                   libspeex
adpcm_xa                eamad                   libvorbis
adpcm_yamaha            eatgq                   libvpx_vp8
aic                     eatgv                   libvpx_vp9
alac                    eatqi                   libzvbi_teletext
alias_pix               eightbps                loco
als                     eightsvx_exp            mace3
amrnb                   eightsvx_fib            mace6
amrwb                   escape124               mdec
amv                     escape130               metasound
anm                     evrc                    microdvd
ansi                    exr                     mimic
ape                     ffv1                    mjpeg
apng                    ffvhuff                 mjpegb
ass                     ffwavesynth             mlp
asv1                    fic                     mmvideo
asv2                    flac                    motionpixels
atrac1                  flashsv                 movtext
atrac3                  flashsv2                mp1
atrac3p                 flic                    mp1float
aura                    flv                     mp2
aura2                   fourxm                  mp2float
avrn                    fraps                   mp3
avrp                    frwu                    mp3adu
avs                     g2m                     mp3adufloat
avui                    g723_1                  mp3float
ayuv                    g729                    mp3on4
bethsoftvid             gif                     mp3on4float
mpc7                    pjs                     tscc
mpc8                    png                     tscc2
mpeg1video              ppm                     tta
mpeg2video              prores                  twinvq
mpeg4                   prores_lgpl             txd
mpegvideo               ptx                     ulti
mpl2                    qcelp                   utvideo
msa1                    qdm2                    v210
msmpeg4v1               qdraw                   v210x
msmpeg4v2               qpeg                    v308
msmpeg4v3               qtrle                   v408
msrle                   r10k                    v410
mss1                    r210                    vb
mss2                    ra_144                  vble
msvideo1                ra_288                  vc1
mszh                    ralf                    vc1image
mts2                    rawvideo                vcr1
mvc1                    realtext                vima
mvc2                    rl2                     vmdaudio
mxpeg                   roq                     vmdvideo
nellymoser              roq_dpcm                vmnc
nuv                     rpza                    vorbis
on2avc                  rv10                    vp3
opus                    rv20                    vp5
paf_audio               rv30                    vp6
paf_video               rv40                    vp6a
pam                     s302m                   vp6f
pbm                     sami                    vp7
pcm_alaw                sanm                    vp8
pcm_bluray              sgi                     vp9
pcm_dvd                 sgirle                  vplayer
pcm_f32be               shorten                 vqa
pcm_f32le               sipr                    wavpack
pcm_f64be               smackaud                webp
pcm_f64le               smacker                 webvtt
pcm_lxf                 smc                     wmalossless
pcm_mulaw               smvjpeg                 wmapro
pcm_s16be               snow                    wmav1
pcm_s16be_planar        sol_dpcm                wmav2
pcm_s16le               sonic                   wmavoice
pcm_s16le_planar        sp5x                    wmv1
pcm_s24be               srt                     wmv2
pcm_s24daud             ssa                     wmv3
pcm_s24le               stl                     wmv3image
pcm_s24le_planar        subrip                  wnv1
pcm_s32be               subviewer               ws_snd1
pcm_s32le               subviewer1              xan_dpcm
pcm_s32le_planar        sunrast                 xan_wc3
pcm_s8                  svq1                    xan_wc4
pcm_s8_planar           svq3                    xbin
pcm_u16be               tak                     xbm
pcm_u16le               targa                   xface
pcm_u24be               targa_y216              xl
pcm_u24le               text                    xsub
pcm_u32be               theora                  xwd
pcm_u32le               thp                     y41p
pcm_u8                  tiertexseqvideo         yop
pcm_zork                tiff                    yuv4
pcx                     tmv                     zero12v
pgm                     truehd                  zerocodec
pgmyuv                  truemotion1             zlib
pgssub                  truemotion2             zmbv
pictor                  truespeech

Enabled encoders:
a64multi                libopenjpeg             pcm_u24le
a64multi5               libopus                 pcm_u32be
aac                     libschroedinger         pcm_u32le
ac3                     libshine                pcm_u8
ac3_fixed               libspeex                pcx
adpcm_adx               libtheora               pgm
adpcm_g722              libtwolame              pgmyuv
adpcm_g726              libvo_amrwbenc          png
adpcm_ima_qt            libvorbis               ppm
adpcm_ima_wav           libvpx_vp8              prores
adpcm_ms                libvpx_vp9              prores_aw
adpcm_swf               libwavpack              prores_ks
adpcm_yamaha            libwebp                 qtrle
alac                    libx264                 r10k
alias_pix               libx264rgb              r210
amv                     libx265                 ra_144
ass                     libxavs                 rawvideo
asv1                    libxvid                 roq
asv2                    ljpeg                   roq_dpcm
avrp                    mjpeg                   rv10
avui                    movtext                 rv20
ayuv                    mp2                     s302m
bmp                     mp2fixed                sgi
cinepak                 mpeg1video              snow
cljr                    mpeg2video              sonic
comfortnoise            mpeg4                   sonic_ls
dca                     msmpeg4v2               srt
dnxhd                   msmpeg4v3               ssa
dpx                     msvideo1                subrip
dvbsub                  nellymoser              sunrast
dvdsub                  pam                     svq1
dvvideo                 pbm                     targa
eac3                    pcm_alaw                tiff
ffv1                    pcm_f32be               tta
ffvhuff                 pcm_f32le               utvideo
flac                    pcm_f64be               v210
flashsv                 pcm_f64le               v308
flashsv2                pcm_mulaw               v408
flv                     pcm_s16be               v410
g723_1                  pcm_s16be_planar        vorbis
gif                     pcm_s16le               wavpack
h261                    pcm_s16le_planar        webvtt
h263                    pcm_s24be               wmav1
h263p                   pcm_s24daud             wmav2
huffyuv                 pcm_s24le               wmv1
jpeg2000                pcm_s24le_planar        wmv2
jpegls                  pcm_s32be               xbm
libaacplus              pcm_s32le               xface
libfaac                 pcm_s32le_planar        xsub
libfdk_aac              pcm_s8                  xwd
libgsm                  pcm_s8_planar           y41p
libgsm_ms               pcm_u16be               yuv4
libilbc                 pcm_u16le               zlib
libmp3lame              pcm_u24be               zmbv
libopencore_amrnb

Enabled hwaccels:

Enabled parsers:
aac                     dvd_nav                 mpegvideo
aac_latm                dvdsub                  opus
ac3                     flac                    png
adx                     gsm                     pnm
bmp                     h261                    rv30
cavsvideo               h263                    rv40
cook                    h264                    tak
dca                     hevc                    vc1
dirac                   mjpeg                   vorbis
dnxhd                   mlp                     vp3
dpx                     mpeg4video              vp8
dvbsub                  mpegaudio               vp9

Enabled demuxers:
aac                     h261                    mvi
ac3                     h263                    mxf
act                     h264                    mxg
adf                     hevc                    nc
adp                     hls                     nistsphere
adx                     hnm                     nsv
aea                     ico                     nut
afc                     idcin                   nuv
aiff                    idf                     ogg
amr                     iff                     oma
anm                     ilbc                    paf
apc                     image2                  pcm_alaw
ape                     image2_alias_pix        pcm_f32be
apng                    image2_brender_pix      pcm_f32le
aqtitle                 image2pipe              pcm_f64be
asf                     image_bmp_pipe          pcm_f64le
ass                     image_dpx_pipe          pcm_mulaw
ast                     image_exr_pipe          pcm_s16be
au                      image_j2k_pipe          pcm_s16le
avi                     image_jpeg_pipe         pcm_s24be
avr                     image_jpegls_pipe       pcm_s24le
avs                     image_pictor_pipe       pcm_s32be
bethsoftvid             image_png_pipe          pcm_s32le
bfi                     image_sgi_pipe          pcm_s8
bink                    image_sunrast_pipe      pcm_u16be
bintext                 image_tiff_pipe         pcm_u16le
bit                     image_webp_pipe         pcm_u24be
bmv                     ingenient               pcm_u24le
boa                     ipmovie                 pcm_u32be
brstm                   ircam                   pcm_u32le
c93                     iss                     pcm_u8
caf                     iv8                     pjs
cavsvideo               ivf                     pmp
cdg                     jacosub                 pva
cdxl                    jv                      pvf
cine                    latm                    qcp
concat                  libmodplug              r3d
data                    libnut                  rawvideo
daud                    live_flv                realtext
dfa                     lmlm4                   redspark
dirac                   loas                    rl2
dnxhd                   lrc                     rm
dsf                     lvf                     roq
dsicin                  lxf                     rpl
dts                     m4v                     rsd
dtshd                   matroska                rso
dv                      mgsts                   rtp
dxa                     microdvd                rtsp
ea                      mjpeg                   sami
ea_cdata                mlp                     sap
eac3                    mlv                     sbg
epaf                    mm                      sdp
ffm                     mmf                     sdr2
ffmetadata              mov                     segafilm
filmstrip               mp3                     shorten
flac                    mpc                     siff
flic                    mpc8                    sln
flv                     mpegps                  smacker
fourxm                  mpegts                  smjpeg
frm                     mpegtsraw               smush
g722                    mpegvideo               sol
g723_1                  mpl2                    sox
g729                    mpsub                   spdif
gif                     msnwc_tcp               srt
gsm                     mtv                     stl
gxf                     mv                      str
subviewer               txd                     webm_dash_manifest
subviewer1              vc1                     webvtt
sup                     vc1t                    wsaud
swf                     vivo                    wsvqa
tak                     vmd                     wtv
tedcaptions             vobsub                  wv
thp                     voc                     xa
tiertexseq              vplayer                 xbin
tmv                     vqf                     xmv
truehd                  w64                     xwma
tta                     wav                     yop
tty                     wc3                     yuv4mpegpipe

Enabled muxers:
a64                     ipod                    pcm_s24be
ac3                     ircam                   pcm_s24le
adts                    ismv                    pcm_s32be
adx                     ivf                     pcm_s32le
aiff                    jacosub                 pcm_s8
amr                     latm                    pcm_u16be
asf                     libnut                  pcm_u16le
asf_stream              lrc                     pcm_u24be
ass                     m4v                     pcm_u24le
ast                     matroska                pcm_u32be
au                      matroska_audio          pcm_u32le
avi                     md5                     pcm_u8
avm2                    microdvd                psp
bit                     mjpeg                   rawvideo
caf                     mkvtimestamp_v2         rm
cavsvideo               mlp                     roq
crc                     mmf                     rso
dash                    mov                     rtp
data                    mp2                     rtsp
daud                    mp3                     sap
dirac                   mp4                     segment
dnxhd                   mpeg1system             smjpeg
dts                     mpeg1vcd                smoothstreaming
dv                      mpeg1video              sox
eac3                    mpeg2dvd                spdif
f4v                     mpeg2svcd               spx
ffm                     mpeg2video              srt
ffmetadata              mpeg2vob                stream_segment
filmstrip               mpegts                  swf
flac                    mpjpeg                  tee
flv                     mxf                     tg2
framecrc                mxf_d10                 tgp
framemd5                null                    truehd
g722                    nut                     uncodedframecrc
g723_1                  oga                     vc1
gif                     ogg                     vc1t
gxf                     oma                     voc
h261                    opus                    w64
h263                    pcm_alaw                wav
h264                    pcm_f32be               webm
hds                     pcm_f32le               webm_dash_manifest
hevc                    pcm_f64be               webp
hls                     pcm_f64le               webvtt
ico                     pcm_mulaw               wtv
ilbc                    pcm_s16be               wv
image2                  pcm_s16le               yuv4mpegpipe
image2pipe

Enabled protocols:
bluray                  httpproxy               mmst
cache                   icecast                 pipe
concat                  librtmp                 rtp
crypto                  librtmpe                srtp
data                    librtmps                subfile
file                    librtmpt                tcp
ftp                     librtmpte               udp
gopher                  md5                     udplite
hls                     mmsh                    unix
http

Enabled filters:
adelay                  delogo                  pad
aecho                   deshake                 pan
aeval                   drawbox                 perms
aevalsrc                drawgrid                perspective
afade                   drawtext                phase
aformat                 earwax                  pixdesctest
ainterleave             ebur128                 pp
allpass                 edgedetect              psnr
alphaextract            elbg                    pullup
alphamerge              equalizer               removelogo
amerge                  extractplanes           replaygain
amix                    fade                    rgbtestsrc
amovie                  field                   rotate
anull                   fieldmatch              sab
anullsink               fieldorder              scale
anullsrc                flanger                 select
apad                    flite                   sendcmd
aperms                  format                  separatefields
aphaser                 fps                     setdar
aresample               framepack               setfield
aselect                 framestep               setpts
asendcmd                frei0r                  setsar
asetnsamples            frei0r_src              settb
asetpts                 geq                     showcqt
asetrate                gradfun                 showinfo
asettb                  haldclut                showspectrum
ashowinfo               haldclutsrc             showwaves
asplit                  hflip                   shuffleplanes
ass                     highpass                signalstats
astats                  histeq                  silencedetect
astreamsync             histogram               silenceremove
atempo                  hqdn3d                  sine
atrim                   hqx                     smartblur
avectorscope            hue                     smptebars
azmq                    idet                    smptehdbars
bandpass                il                      split
bandreject              interlace               spp
bass                    interleave              stereo3d
bbox                    join                    subtitles
biquad                  kerndeint               super2xsai
blackdetect             lenscorrection          swapuv
blackframe              life                    telecine
blend                   lowpass                 testsrc
boxblur                 lut                     thumbnail
bs2b                    lut3d                   tile
cellauto                lutrgb                  tinterlace
channelmap              lutyuv                  transpose
channelsplit            mandelbrot              treble
codecview               mcdeint                 trim
color                   mergeplanes             unsharp
colorbalance            movie                   vflip
colorchannelmixer       mp                      vidstabdetect
colormatrix             mpdecimate              vidstabtransform
compand                 mptestsrc               vignette
concat                  negate                  volume
copy                    noformat                volumedetect
crop                    noise                   w3fdif
cropdetect              null                    xbr
curves                  nullsink                yadif
dctdnoiz                nullsrc                 zmq
decimate                overlay                 zoompan
dejudder                owdenoise

Enabled bsfs:
aac_adtstoasc           imx_dump_header         mp3_header_decompress
chomp                   mjpeg2jpeg              noise
dump_extradata          mjpega_dump_header      remove_extradata
h264_mp4toannexb        mov2textsub             text2movsub

Enabled indevs:
dv1394                  lavfi                   oss
fbdev                   libcdio                 v4l2
iec61883                libdc1394

Enabled outdevs:
caca                    oss                     v4l2
fbdev
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
