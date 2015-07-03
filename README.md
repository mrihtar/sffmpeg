This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more external
libraries included.

Static **ffmpeg v2.7.1** build from this repository currently compiles on:
<table>
<tr><td><b>CentOS 6.6</b>      </td><td>i386 and x86_64</td>
<td rowspan="3">
<img src="http://www.movieconverter-studio.com/_PUBLIC/ffmpeg/logo-new/ffmpeg-logo-src/ffmpeg-logo.png" height="90">
</td></tr>
<tr><td><b>Ubuntu 14.04.2 LTS</b></td><td>i386 and x86_64</td></tr>
<tr><td><b>Debian 7.8</b>      </td><td>i386 and x86_64</td></tr>
</table>

For build see [BUILD.md].

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            2.7.1
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
aac                     bfi                     g729
aac_latm                bink                    gif
aasc                    binkaudio_dct           gsm
ac3                     binkaudio_rdft          gsm_ms
ac3_fixed               bintext                 h261
adpcm_4xm               bmp                     h263
adpcm_adx               bmv_audio               h263i
adpcm_afc               bmv_video               h263p
adpcm_ct                brender_pix             h264
adpcm_dtk               c93                     hevc
adpcm_ea                cavs                    hnm4_video
adpcm_ea_maxis_xa       ccaption                hq_hqa
adpcm_ea_r1             cdgraphics              hqx
adpcm_ea_r2             cdxl                    huffyuv
adpcm_ea_r3             cinepak                 iac
adpcm_ea_xas            cljr                    idcin
adpcm_g722              cllc                    idf
adpcm_g726              comfortnoise            iff_byterun1
adpcm_g726le            cook                    iff_ilbm
adpcm_ima_amv           cpia                    imc
adpcm_ima_apc           cscd                    indeo2
adpcm_ima_dk3           cyuv                    indeo3
adpcm_ima_dk4           dca                     indeo4
adpcm_ima_ea_eacs       dfa                     indeo5
adpcm_ima_ea_sead       dirac                   interplay_dpcm
adpcm_ima_iss           dnxhd                   interplay_video
adpcm_ima_oki           dpx                     jacosub
adpcm_ima_qt            dsd_lsbf                jpeg2000
adpcm_ima_rad           dsd_lsbf_planar         jpegls
adpcm_ima_smjpeg        dsd_msbf                jv
adpcm_ima_wav           dsd_msbf_planar         kgv1
adpcm_ima_ws            dsicinaudio             kmvc
adpcm_ms                dsicinvideo             lagarith
adpcm_sbpro_2           dss_sp                  libfdk_aac
adpcm_sbpro_3           dvbsub                  libgsm
adpcm_sbpro_4           dvdsub                  libgsm_ms
adpcm_swf               dvvideo                 libilbc
adpcm_thp               dxa                     libopencore_amrnb
adpcm_vima              dxtory                  libopencore_amrwb
adpcm_xa                eac3                    libopenjpeg
adpcm_yamaha            eacmv                   libopus
aic                     eamad                   libschroedinger
alac                    eatgq                   libspeex
alias_pix               eatgv                   libvorbis
als                     eatqi                   libvpx_vp8
amrnb                   eightbps                libvpx_vp9
amrwb                   eightsvx_exp            libzvbi_teletext
amv                     eightsvx_fib            loco
anm                     escape124               mace3
ansi                    escape130               mace6
ape                     evrc                    mdec
apng                    exr                     metasound
ass                     ffv1                    microdvd
asv1                    ffvhuff                 mimic
asv2                    ffwavesynth             mjpeg
atrac1                  fic                     mjpegb
atrac3                  flac                    mlp
atrac3p                 flashsv                 mmvideo
aura                    flashsv2                motionpixels
aura2                   flic                    movtext
avrn                    flv                     mp1
avrp                    fourxm                  mp1float
avs                     fraps                   mp2
avui                    frwu                    mp2float
ayuv                    g2m                     mp3
bethsoftvid             g723_1                  mp3adu
mp3adufloat             pgssub                  truemotion2
mp3float                pictor                  truespeech
mp3on4                  pjs                     tscc
mp3on4float             png                     tscc2
mpc7                    ppm                     tta
mpc8                    prores                  twinvq
mpeg1video              prores_lgpl             txd
mpeg2video              ptx                     ulti
mpeg4                   qcelp                   utvideo
mpegvideo               qdm2                    v210
mpl2                    qdraw                   v210x
msa1                    qpeg                    v308
msmpeg4v1               qtrle                   v408
msmpeg4v2               r10k                    v410
msmpeg4v3               r210                    vb
msrle                   ra_144                  vble
mss1                    ra_288                  vc1
mss2                    ralf                    vc1image
msvideo1                rawvideo                vcr1
mszh                    realtext                vima
mts2                    rl2                     vmdaudio
mvc1                    roq                     vmdvideo
mvc2                    roq_dpcm                vmnc
mxpeg                   rpza                    vorbis
nellymoser              rv10                    vp3
nuv                     rv20                    vp5
on2avc                  rv30                    vp6
opus                    rv40                    vp6a
paf_audio               s302m                   vp6f
paf_video               sami                    vp7
pam                     sanm                    vp8
pbm                     sgi                     vp9
pcm_alaw                sgirle                  vplayer
pcm_bluray              shorten                 vqa
pcm_dvd                 sipr                    wavpack
pcm_f32be               smackaud                webp
pcm_f32le               smacker                 webvtt
pcm_f64be               smc                     wmalossless
pcm_f64le               smvjpeg                 wmapro
pcm_lxf                 snow                    wmav1
pcm_mulaw               sol_dpcm                wmav2
pcm_s16be               sonic                   wmavoice
pcm_s16be_planar        sp5x                    wmv1
pcm_s16le               srt                     wmv2
pcm_s16le_planar        ssa                     wmv3
pcm_s24be               stl                     wmv3image
pcm_s24daud             subrip                  wnv1
pcm_s24le               subviewer               ws_snd1
pcm_s24le_planar        subviewer1              xan_dpcm
pcm_s32be               sunrast                 xan_wc3
pcm_s32le               svq1                    xan_wc4
pcm_s32le_planar        svq3                    xbin
pcm_s8                  tak                     xbm
pcm_s8_planar           targa                   xface
pcm_u16be               targa_y216              xl
pcm_u16le               tdsc                    xsub
pcm_u24be               text                    xwd
pcm_u24le               theora                  y41p
pcm_u32be               thp                     yop
pcm_u32le               tiertexseqvideo         yuv4
pcm_u8                  tiff                    zero12v
pcm_zork                tmv                     zerocodec
pcx                     truehd                  zlib
pgm                     truemotion1             zmbv
pgmyuv

Enabled encoders:
a64multi                libopencore_amrnb       pcm_u24le
a64multi5               libopenjpeg             pcm_u32be
aac                     libopus                 pcm_u32le
ac3                     libschroedinger         pcm_u8
ac3_fixed               libshine                pcx
adpcm_adx               libspeex                pgm
adpcm_g722              libtheora               pgmyuv
adpcm_g726              libtwolame              png
adpcm_ima_qt            libvo_amrwbenc          ppm
adpcm_ima_wav           libvorbis               prores
adpcm_ms                libvpx_vp8              prores_aw
adpcm_swf               libvpx_vp9              prores_ks
adpcm_yamaha            libwavpack              qtrle
alac                    libwebp                 r10k
alias_pix               libx264                 r210
amv                     libx264rgb              ra_144
apng                    libx265                 rawvideo
ass                     libxavs                 roq
asv1                    libxvid                 roq_dpcm
asv2                    ljpeg                   rv10
avrp                    mjpeg                   rv20
avui                    movtext                 s302m
ayuv                    mp2                     sgi
bmp                     mp2fixed                snow
cinepak                 mpeg1video              sonic
cljr                    mpeg2video              sonic_ls
comfortnoise            mpeg4                   srt
dca                     msmpeg4v2               ssa
dnxhd                   msmpeg4v3               subrip
dpx                     msvideo1                sunrast
dvbsub                  nellymoser              svq1
dvdsub                  pam                     targa
dvvideo                 pbm                     tiff
eac3                    pcm_alaw                tta
ffv1                    pcm_f32be               utvideo
ffvhuff                 pcm_f32le               v210
flac                    pcm_f64be               v308
flashsv                 pcm_f64le               v408
flashsv2                pcm_mulaw               v410
flv                     pcm_s16be               vorbis
g723_1                  pcm_s16be_planar        wavpack
gif                     pcm_s16le               webvtt
h261                    pcm_s16le_planar        wmav1
h263                    pcm_s24be               wmav2
h263p                   pcm_s24daud             wmv1
huffyuv                 pcm_s24le               wmv2
jpeg2000                pcm_s24le_planar        xbm
jpegls                  pcm_s32be               xface
libaacplus              pcm_s32le               xsub
libfaac                 pcm_s32le_planar        xwd
libfdk_aac              pcm_s8                  y41p
libgsm                  pcm_s8_planar           yuv4
libgsm_ms               pcm_u16be               zlib
libilbc                 pcm_u16le               zmbv
libmp3lame              pcm_u24be

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
aac                     gsm                     mpsub
ac3                     gxf                     msnwc_tcp
act                     h261                    mtv
adf                     h263                    mv
adp                     h264                    mvi
adx                     hevc                    mxf
aea                     hls                     mxg
afc                     hnm                     nc
aiff                    ico                     nistsphere
amr                     idcin                   nsv
anm                     idf                     nut
apc                     iff                     nuv
ape                     ilbc                    ogg
apng                    image2                  oma
aqtitle                 image2_alias_pix        paf
asf                     image2_brender_pix      pcm_alaw
ass                     image2pipe              pcm_f32be
ast                     image_bmp_pipe          pcm_f32le
au                      image_dpx_pipe          pcm_f64be
avi                     image_exr_pipe          pcm_f64le
avr                     image_j2k_pipe          pcm_mulaw
avs                     image_jpeg_pipe         pcm_s16be
bethsoftvid             image_jpegls_pipe       pcm_s16le
bfi                     image_pictor_pipe       pcm_s24be
bink                    image_png_pipe          pcm_s24le
bintext                 image_qdraw_pipe        pcm_s32be
bit                     image_sgi_pipe          pcm_s32le
bmv                     image_sunrast_pipe      pcm_s8
boa                     image_tiff_pipe         pcm_u16be
brstm                   image_webp_pipe         pcm_u16le
c93                     ingenient               pcm_u24be
caf                     ipmovie                 pcm_u24le
cavsvideo               ircam                   pcm_u32be
cdg                     iss                     pcm_u32le
cdxl                    iv8                     pcm_u8
cine                    ivf                     pjs
concat                  jacosub                 pmp
data                    jv                      pva
daud                    latm                    pvf
dfa                     libmodplug              qcp
dirac                   libnut                  r3d
dnxhd                   live_flv                rawvideo
dsf                     lmlm4                   realtext
dsicin                  loas                    redspark
dss                     lrc                     rl2
dts                     lvf                     rm
dtshd                   lxf                     roq
dv                      m4v                     rpl
dvbsub                  matroska                rsd
dxa                     mgsts                   rso
ea                      microdvd                rtp
ea_cdata                mjpeg                   rtsp
eac3                    mlp                     sami
epaf                    mlv                     sap
ffm                     mm                      sbg
ffmetadata              mmf                     sdp
filmstrip               mov                     sdr2
flac                    mp3                     segafilm
flic                    mpc                     shorten
flv                     mpc8                    siff
fourxm                  mpegps                  sln
frm                     mpegts                  smacker
g722                    mpegtsraw               smjpeg
g723_1                  mpegvideo               smush
g729                    mpjpeg                  sol
gif                     mpl2                    sox
spdif                   tta                     wc3
srt                     tty                     webm_dash_manifest
stl                     txd                     webvtt
str                     vc1                     wsaud
subviewer               vc1t                    wsvqa
subviewer1              vivo                    wtv
sup                     vmd                     wv
swf                     vobsub                  xa
tak                     voc                     xbin
tedcaptions             vplayer                 xmv
thp                     vqf                     xwma
tiertexseq              w64                     yop
tmv                     wav                     yuv4mpegpipe
truehd

Enabled muxers:
a64                     ipod                    pcm_s24le
ac3                     ircam                   pcm_s32be
adts                    ismv                    pcm_s32le
adx                     ivf                     pcm_s8
aiff                    jacosub                 pcm_u16be
amr                     latm                    pcm_u16le
apng                    libnut                  pcm_u24be
asf                     lrc                     pcm_u24le
asf_stream              m4v                     pcm_u32be
ass                     matroska                pcm_u32le
ast                     matroska_audio          pcm_u8
au                      md5                     psp
avi                     microdvd                rawvideo
avm2                    mjpeg                   rm
bit                     mkvtimestamp_v2         roq
caf                     mlp                     rso
cavsvideo               mmf                     rtp
crc                     mov                     rtp_mpegts
dash                    mp2                     rtsp
data                    mp3                     sap
daud                    mp4                     segment
dirac                   mpeg1system             singlejpeg
dnxhd                   mpeg1vcd                smjpeg
dts                     mpeg1video              smoothstreaming
dv                      mpeg2dvd                sox
eac3                    mpeg2svcd               spdif
f4v                     mpeg2video              spx
ffm                     mpeg2vob                srt
ffmetadata              mpegts                  stream_segment
filmstrip               mpjpeg                  swf
flac                    mxf                     tee
flv                     mxf_d10                 tg2
framecrc                mxf_opatom              tgp
framemd5                null                    truehd
g722                    nut                     uncodedframecrc
g723_1                  oga                     vc1
gif                     ogg                     vc1t
gxf                     oma                     voc
h261                    opus                    w64
h263                    pcm_alaw                wav
h264                    pcm_f32be               webm
hds                     pcm_f32le               webm_chunk
hevc                    pcm_f64be               webm_dash_manifest
hls                     pcm_f64le               webp
ico                     pcm_mulaw               webvtt
ilbc                    pcm_s16be               wtv
image2                  pcm_s16le               wv
image2pipe              pcm_s24be               yuv4mpegpipe

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
aecho                   deshake                 palettegen
aeval                   detelecine              paletteuse
aevalsrc                drawbox                 pan
afade                   drawgrid                perms
aformat                 drawtext                perspective
ainterleave             earwax                  phase
allpass                 ebur128                 pixdesctest
alphaextract            edgedetect              pp
alphamerge              elbg                    pp7
amerge                  eq                      psnr
amix                    equalizer               pullup
amovie                  extractplanes           qp
anull                   fade                    removelogo
anullsink               fftfilt                 repeatfields
anullsrc                field                   replaygain
apad                    fieldmatch              rgbtestsrc
aperms                  fieldorder              rotate
aphaser                 find_rect               sab
aresample               flanger                 scale
aselect                 flite                   select
asendcmd                format                  sendcmd
asetnsamples            fps                     separatefields
asetpts                 framepack               setdar
asetrate                framestep               setfield
asettb                  frei0r                  setpts
ashowinfo               frei0r_src              setsar
asplit                  fspp                    settb
ass                     geq                     showcqt
astats                  gradfun                 showinfo
astreamsync             haldclut                showpalette
atempo                  haldclutsrc             showspectrum
atrim                   hflip                   showwaves
avectorscope            highpass                showwavespic
azmq                    histeq                  shuffleplanes
bandpass                histogram               signalstats
bandreject              hqdn3d                  silencedetect
bass                    hqx                     silenceremove
bbox                    hue                     sine
biquad                  idet                    smartblur
blackdetect             il                      smptebars
blackframe              interlace               smptehdbars
blend                   interleave              split
boxblur                 join                    spp
bs2b                    kerndeint               stereo3d
cellauto                lenscorrection          subtitles
channelmap              life                    super2xsai
channelsplit            lowpass                 swapuv
chorus                  lut                     tblend
codecview               lut3d                   telecine
color                   lutrgb                  testsrc
colorbalance            lutyuv                  thumbnail
colorchannelmixer       mandelbrot              tile
colorlevels             mcdeint                 tinterlace
colormatrix             mergeplanes             transpose
compand                 movie                   treble
concat                  mpdecimate              trim
copy                    mptestsrc               unsharp
cover_rect              negate                  uspp
crop                    noformat                vflip
cropdetect              noise                   vidstabdetect
curves                  null                    vidstabtransform
dcshift                 nullsink                vignette
dctdnoiz                nullsrc                 volume
decimate                overlay                 volumedetect
dejudder                owdenoise               w3fdif
xbr                     zmq                     zoompan
yadif

Enabled bsfs:
aac_adtstoasc           mjpeg2jpeg              mpeg4_unpack_bframes
chomp                   mjpega_dump_header      noise
dump_extradata          mov2textsub             remove_extradata
h264_mp4toannexb        mp3_header_decompress   text2movsub
imx_dump_header

Enabled indevs:
dv1394                  lavfi                   oss
fbdev                   libcdio                 v4l2
iec61883                libdc1394

Enabled outdevs:
caca                    oss                     v4l2
fbdev
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
