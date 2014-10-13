This repository is an extended clone of https://github.com/pyke369/sffmpeg<br>
It builds a static version of ffmpeg executable with a lot of external libraries included.

Static ffmpeg build from this repository currently compiles on:
<table>
<tr><td><b>CentOS 6.5</b></td><td>i386 and x86_64</td></tr>
<tr><td><b>Ubuntu 14.04 LTS</b></td><td>i386 and x86_64</td></tr>
<tr><td><b>Debian 7.6</b></td><td>i386 and x86_64</td></tr>
</table>

For build see BUILD.md.

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            2.4.2
C compiler                gcc
runtime cpu detection     yes
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
CMOV is fast              yes
EBX available             yes
EBP available             yes
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
aac                     bink                    gsm_ms
aac_latm                binkaudio_dct           h261
aasc                    binkaudio_rdft          h263
ac3                     bintext                 h263i
ac3_fixed               bmp                     h263p
adpcm_4xm               bmv_audio               h264
adpcm_adx               bmv_video               hevc
adpcm_afc               brender_pix             hnm4_video
adpcm_ct                c93                     huffyuv
adpcm_dtk               cavs                    iac
adpcm_ea                cdgraphics              idcin
adpcm_ea_maxis_xa       cdxl                    idf
adpcm_ea_r1             cinepak                 iff_byterun1
adpcm_ea_r2             cljr                    iff_ilbm
adpcm_ea_r3             cllc                    imc
adpcm_ea_xas            comfortnoise            indeo2
adpcm_g722              cook                    indeo3
adpcm_g726              cpia                    indeo4
adpcm_g726le            cscd                    indeo5
adpcm_ima_amv           cyuv                    interplay_dpcm
adpcm_ima_apc           dca                     interplay_video
adpcm_ima_dk3           dfa                     jacosub
adpcm_ima_dk4           dirac                   jpeg2000
adpcm_ima_ea_eacs       dnxhd                   jpegls
adpcm_ima_ea_sead       dpx                     jv
adpcm_ima_iss           dsd_lsbf                kgv1
adpcm_ima_oki           dsd_lsbf_planar         kmvc
adpcm_ima_qt            dsd_msbf                lagarith
adpcm_ima_rad           dsd_msbf_planar         libfdk_aac
adpcm_ima_smjpeg        dsicinaudio             libgsm
adpcm_ima_wav           dsicinvideo             libgsm_ms
adpcm_ima_ws            dvbsub                  libilbc
adpcm_ms                dvdsub                  libopencore_amrnb
adpcm_sbpro_2           dvvideo                 libopencore_amrwb
adpcm_sbpro_3           dxa                     libopenjpeg
adpcm_sbpro_4           dxtory                  libopus
adpcm_swf               eac3                    libschroedinger
adpcm_thp               eacmv                   libspeex
adpcm_vima              eamad                   libvorbis
adpcm_xa                eatgq                   libvpx_vp8
adpcm_yamaha            eatgv                   libvpx_vp9
aic                     eatqi                   libzvbi_teletext
alac                    eightbps                loco
alias_pix               eightsvx_exp            mace3
als                     eightsvx_fib            mace6
amrnb                   escape124               mdec
amrwb                   escape130               metasound
amv                     evrc                    microdvd
anm                     exr                     mimic
ansi                    ffv1                    mjpeg
ape                     ffvhuff                 mjpegb
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
bfi                     gsm                     mpc7
mpc8                    pjs                     tscc
mpeg1video              png                     tscc2
mpeg2video              ppm                     tta
mpeg4                   prores                  twinvq
mpegvideo               prores_lgpl             txd
mpl2                    ptx                     ulti
msa1                    qcelp                   utvideo
msmpeg4v1               qdm2                    v210
msmpeg4v2               qdraw                   v210x
msmpeg4v3               qpeg                    v308
msrle                   qtrle                   v408
mss1                    r10k                    v410
mss2                    r210                    vb
msvideo1                ra_144                  vble
mszh                    ra_288                  vc1
mts2                    ralf                    vc1image
mvc1                    rawvideo                vcr1
mvc2                    realtext                vima
mxpeg                   rl2                     vmdaudio
nellymoser              roq                     vmdvideo
nuv                     roq_dpcm                vmnc
on2avc                  rpza                    vorbis
opus                    rv10                    vp3
paf_audio               rv20                    vp5
paf_video               rv30                    vp6
pam                     rv40                    vp6a
pbm                     s302m                   vp6f
pcm_alaw                sami                    vp7
pcm_bluray              sanm                    vp8
pcm_dvd                 sgi                     vp9
pcm_f32be               sgirle                  vplayer
pcm_f32le               shorten                 vqa
pcm_f64be               sipr                    wavpack
pcm_f64le               smackaud                webp
pcm_lxf                 smacker                 webvtt
pcm_mulaw               smc                     wmalossless
pcm_s16be               smvjpeg                 wmapro
pcm_s16be_planar        snow                    wmav1
pcm_s16le               sol_dpcm                wmav2
pcm_s16le_planar        sonic                   wmavoice
pcm_s24be               sp5x                    wmv1
pcm_s24daud             srt                     wmv2
pcm_s24le               ssa                     wmv3
pcm_s24le_planar        subrip                  wmv3image
pcm_s32be               subviewer               wnv1
pcm_s32le               subviewer1              ws_snd1
pcm_s32le_planar        sunrast                 xan_dpcm
pcm_s8                  svq1                    xan_wc3
pcm_s8_planar           svq3                    xan_wc4
pcm_u16be               tak                     xbin
pcm_u16le               targa                   xbm
pcm_u24be               targa_y216              xface
pcm_u24le               text                    xl
pcm_u32be               theora                  xsub
pcm_u32le               thp                     xwd
pcm_u8                  tiertexseqvideo         y41p
pcm_zork                tiff                    yop
pcx                     tmv                     yuv4
pgm                     truehd                  zero12v
pgmyuv                  truemotion1             zerocodec
pgssub                  truemotion2             zlib
pictor                  truespeech              zmbv

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
aac                     h263                    mxg
ac3                     h264                    nc
act                     hevc                    nistsphere
adf                     hls                     nsv
adp                     hnm                     nut
adx                     ico                     nuv
aea                     idcin                   ogg
afc                     idf                     oma
aiff                    iff                     paf
amr                     ilbc                    pcm_alaw
anm                     image2                  pcm_f32be
apc                     image2_alias_pix        pcm_f32le
ape                     image2_brender_pix      pcm_f64be
aqtitle                 image2pipe              pcm_f64le
asf                     image_bmp_pipe          pcm_mulaw
ass                     image_dpx_pipe          pcm_s16be
ast                     image_exr_pipe          pcm_s16le
au                      image_j2k_pipe          pcm_s24be
avi                     image_jpegls_pipe       pcm_s24le
avr                     image_pictor_pipe       pcm_s32be
avs                     image_png_pipe          pcm_s32le
bethsoftvid             image_sgi_pipe          pcm_s8
bfi                     image_sunrast_pipe      pcm_u16be
bink                    image_tiff_pipe         pcm_u16le
bintext                 image_webp_pipe         pcm_u24be
bit                     ingenient               pcm_u24le
bmv                     ipmovie                 pcm_u32be
boa                     ircam                   pcm_u32le
brstm                   iss                     pcm_u8
c93                     iv8                     pjs
caf                     ivf                     pmp
cavsvideo               jacosub                 pva
cdg                     jv                      pvf
cdxl                    latm                    qcp
cine                    libmodplug              r3d
concat                  libnut                  rawvideo
data                    live_flv                realtext
daud                    lmlm4                   redspark
dfa                     loas                    rl2
dirac                   lrc                     rm
dnxhd                   lvf                     roq
dsf                     lxf                     rpl
dsicin                  m4v                     rsd
dts                     matroska                rso
dtshd                   mgsts                   rtp
dv                      microdvd                rtsp
dxa                     mjpeg                   sami
ea                      mlp                     sap
ea_cdata                mlv                     sbg
eac3                    mm                      sdp
epaf                    mmf                     sdr2
ffm                     mov                     segafilm
ffmetadata              mp3                     shorten
filmstrip               mpc                     siff
flac                    mpc8                    sln
flic                    mpegps                  smacker
flv                     mpegts                  smjpeg
fourxm                  mpegtsraw               smush
frm                     mpegvideo               sol
g722                    mpl2                    sox
g723_1                  mpsub                   spdif
g729                    msnwc_tcp               srt
gif                     mtv                     str
gsm                     mv                      subviewer
gxf                     mvi                     subviewer1
h261                    mxf                     swf
tak                     vivo                    wsaud
tedcaptions             vmd                     wsvqa
thp                     vobsub                  wtv
tiertexseq              voc                     wv
tmv                     vplayer                 xa
truehd                  vqf                     xbin
tta                     w64                     xmv
tty                     wav                     xwma
txd                     wc3                     yop
vc1                     webm_dash_manifest      yuv4mpegpipe
vc1t                    webvtt

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
data                    mov                     rtp
daud                    mp2                     rtsp
dirac                   mp3                     sap
dnxhd                   mp4                     segment
dts                     mpeg1system             smjpeg
dv                      mpeg1vcd                smoothstreaming
eac3                    mpeg1video              sox
f4v                     mpeg2dvd                spdif
ffm                     mpeg2svcd               spx
ffmetadata              mpeg2video              srt
filmstrip               mpeg2vob                stream_segment
flac                    mpegts                  swf
flv                     mpjpeg                  tee
framecrc                mxf                     tg2
framemd5                mxf_d10                 tgp
g722                    null                    truehd
g723_1                  nut                     uncodedframecrc
gif                     oga                     vc1
gxf                     ogg                     vc1t
h261                    oma                     voc
h263                    opus                    w64
h264                    pcm_alaw                wav
hds                     pcm_f32be               webm
hevc                    pcm_f32le               webm_dash_manifest
hls                     pcm_f64be               webvtt
ico                     pcm_f64le               wtv
ilbc                    pcm_mulaw               wv
image2                  pcm_s16be               yuv4mpegpipe
image2pipe              pcm_s16le

Enabled protocols:
bluray                  http                    mmsh
cache                   httpproxy               mmst
concat                  icecast                 pipe
crypto                  librtmp                 rtp
data                    librtmpe                srtp
file                    librtmps                subfile
ftp                     librtmpt                tcp
gopher                  librtmpte               udp
hls                     md5                     unix

Enabled filters:
aconvert                dejudder                owdenoise
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
cropdetect              null                    yadif
curves                  nullsink                zmq
dctdnoiz                nullsrc                 zoompan
decimate                overlay

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
