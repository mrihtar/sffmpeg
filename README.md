This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more external
libraries included.

Static <b>ffmpeg v3.2.2</b> build from this repository currently compiles on:
<table>
<tr><td><b>CentOS 6.8</b>        </td><td>i386 and x86_64</td>
<td rowspan="3">
<img src="http://www.movieconverter-studio.com/_PUBLIC/ffmpeg/logo-new/ffmpeg-logo-src/ffmpeg-logo.png" height="90">
</td></tr>
<tr><td><b>Ubuntu 14.04.5 LTS</b></td><td>i386 and x86_64</td></tr>
<tr><td><b>Debian 7.11</b>       </td><td>i386 and x86_64</td></tr>
</table>

For build see [BUILD.md].

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            3.2.2
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
AESNI enabled             yes
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
SDL2 support              no
opencl enabled            no
JNI support               no
texi2html enabled         no
perl enabled              yes
pod2man enabled           yes
makeinfo enabled          no
makeinfo supports HTML    no

External libraries:
bzlib                   libilbc                 libv4l2
frei0r                  libmodplug              libvidstab
iconv                   libmp3lame              libvo_amrwbenc
libass                  libnut                  libvorbis
libbluray               libopencore_amrnb       libvpx
libbs2b                 libopencore_amrwb       libwavpack
libcaca                 libopenjpeg             libwebp
libcdio                 libopus                 libx264
libdc1394               librtmp                 libx265
libfdk_aac              libschroedinger         libxavs
libflite                libshine                libxvid
libfontconfig           libsoxr                 libzmq
libfreetype             libspeex                libzvbi
libgsm                  libtheora               lzma
libiec61883             libtwolame              zlib

External libraries providing hardware acceleration:
nvenc

Libraries:
avcodec                 avformat                swresample
avdevice                avutil                  swscale
avfilter                postproc

Enabled decoders:
aac                     avrn                    fic
aac_fixed               avrp                    flac
aac_latm                avs                     flashsv
aasc                    avui                    flashsv2
ac3                     ayuv                    flic
ac3_fixed               bethsoftvid             flv
adpcm_4xm               bfi                     fourxm
adpcm_adx               bink                    fraps
adpcm_afc               binkaudio_dct           frwu
adpcm_aica              binkaudio_rdft          g2m
adpcm_ct                bintext                 g723_1
adpcm_dtk               bmp                     g729
adpcm_ea                bmv_audio               gif
adpcm_ea_maxis_xa       bmv_video               gsm
adpcm_ea_r1             brender_pix             gsm_ms
adpcm_ea_r2             c93                     h261
adpcm_ea_r3             cavs                    h263
adpcm_ea_xas            ccaption                h263i
adpcm_g722              cdgraphics              h263p
adpcm_g726              cdxl                    h264
adpcm_g726le            cfhd                    hap
adpcm_ima_amv           cinepak                 hevc
adpcm_ima_apc           cljr                    hnm4_video
adpcm_ima_dat4          cllc                    hq_hqa
adpcm_ima_dk3           comfortnoise            hqx
adpcm_ima_dk4           cook                    huffyuv
adpcm_ima_ea_eacs       cpia                    iac
adpcm_ima_ea_sead       cscd                    idcin
adpcm_ima_iss           cyuv                    idf
adpcm_ima_oki           dca                     iff_ilbm
adpcm_ima_qt            dds                     imc
adpcm_ima_rad           dfa                     indeo2
adpcm_ima_smjpeg        dirac                   indeo3
adpcm_ima_wav           dnxhd                   indeo4
adpcm_ima_ws            dpx                     indeo5
adpcm_ms                dsd_lsbf                interplay_acm
adpcm_mtaf              dsd_lsbf_planar         interplay_dpcm
adpcm_psx               dsd_msbf                interplay_video
adpcm_sbpro_2           dsd_msbf_planar         jacosub
adpcm_sbpro_3           dsicinaudio             jpeg2000
adpcm_sbpro_4           dsicinvideo             jpegls
adpcm_swf               dss_sp                  jv
adpcm_thp               dst                     kgv1
adpcm_thp_le            dvaudio                 kmvc
adpcm_vima              dvbsub                  lagarith
adpcm_xa                dvdsub                  libfdk_aac
adpcm_yamaha            dvvideo                 libgsm
aic                     dxa                     libgsm_ms
alac                    dxtory                  libilbc
alias_pix               dxv                     libopencore_amrnb
als                     eac3                    libopencore_amrwb
amrnb                   eacmv                   libopenjpeg
amrwb                   eamad                   libopus
amv                     eatgq                   libschroedinger
anm                     eatgv                   libspeex
ansi                    eatqi                   libvorbis
ape                     eightbps                libvpx_vp8
apng                    eightsvx_exp            libvpx_vp9
ass                     eightsvx_fib            libzvbi_teletext
asv1                    escape124               loco
asv2                    escape130               m101
atrac1                  evrc                    mace3
atrac3                  exr                     mace6
atrac3p                 ffv1                    magicyuv
aura                    ffvhuff                 mdec
aura2                   ffwavesynth             metasound
microdvd                pcm_s64be               subviewer
mimic                   pcm_s64le               subviewer1
mjpeg                   pcm_s8                  sunrast
mjpegb                  pcm_s8_planar           svq1
mlp                     pcm_u16be               svq3
mmvideo                 pcm_u16le               tak
motionpixels            pcm_u24be               targa
movtext                 pcm_u24le               targa_y216
mp1                     pcm_u32be               tdsc
mp1float                pcm_u32le               text
mp2                     pcm_u8                  theora
mp2float                pcm_zork                thp
mp3                     pcx                     tiertexseqvideo
mp3adu                  pgm                     tiff
mp3adufloat             pgmyuv                  tmv
mp3float                pgssub                  truehd
mp3on4                  pictor                  truemotion1
mp3on4float             pjs                     truemotion2
mpc7                    png                     truemotion2rt
mpc8                    ppm                     truespeech
mpeg1video              prores                  tscc
mpeg2video              prores_lgpl             tscc2
mpeg4                   ptx                     tta
mpegvideo               qcelp                   twinvq
mpl2                    qdm2                    txd
msa1                    qdraw                   ulti
msmpeg4v1               qpeg                    utvideo
msmpeg4v2               qtrle                   v210
msmpeg4v3               r10k                    v210x
msrle                   r210                    v308
mss1                    ra_144                  v408
mss2                    ra_288                  v410
msvideo1                ralf                    vb
mszh                    rawvideo                vble
mts2                    realtext                vc1
mvc1                    rl2                     vc1image
mvc2                    roq                     vcr1
mxpeg                   roq_dpcm                vmdaudio
nellymoser              rpza                    vmdvideo
nuv                     rscc                    vmnc
on2avc                  rv10                    vorbis
opus                    rv20                    vp3
paf_audio               rv30                    vp5
paf_video               rv40                    vp6
pam                     s302m                   vp6a
pbm                     sami                    vp6f
pcm_alaw                sanm                    vp7
pcm_bluray              screenpresso            vp8
pcm_dvd                 sdx2_dpcm               vp9
pcm_f32be               sgi                     vplayer
pcm_f32le               sgirle                  vqa
pcm_f64be               sheervideo              wavpack
pcm_f64le               shorten                 webp
pcm_lxf                 sipr                    webvtt
pcm_mulaw               smackaud                wmalossless
pcm_s16be               smacker                 wmapro
pcm_s16be_planar        smc                     wmav1
pcm_s16le               smvjpeg                 wmav2
pcm_s16le_planar        snow                    wmavoice
pcm_s24be               sol_dpcm                wmv1
pcm_s24daud             sonic                   wmv2
pcm_s24le               sp5x                    wmv3
pcm_s24le_planar        srt                     wmv3image
pcm_s32be               ssa                     wnv1
pcm_s32le               stl                     ws_snd1
pcm_s32le_planar        subrip                  xan_dpcm
xan_wc3                 xma1                    yop
xan_wc4                 xma2                    yuv4
xbin                    xsub                    zero12v
xbm                     xwd                     zerocodec
xface                   y41p                    zlib
xl                      ylc                     zmbv

Enabled encoders:
a64multi                libschroedinger         pcm_u24le
a64multi5               libshine                pcm_u32be
aac                     libspeex                pcm_u32le
ac3                     libtheora               pcm_u8
ac3_fixed               libtwolame              pcx
adpcm_adx               libvo_amrwbenc          pgm
adpcm_g722              libvorbis               pgmyuv
adpcm_g726              libvpx_vp8              png
adpcm_ima_qt            libvpx_vp9              ppm
adpcm_ima_wav           libwavpack              prores
adpcm_ms                libwebp                 prores_aw
adpcm_swf               libx264                 prores_ks
adpcm_yamaha            libx264rgb              qtrle
alac                    libx265                 r10k
alias_pix               libxavs                 r210
amv                     libxvid                 ra_144
apng                    ljpeg                   rawvideo
ass                     mjpeg                   roq
asv1                    mlp                     roq_dpcm
asv2                    movtext                 rv10
avrp                    mp2                     rv20
avui                    mp2fixed                s302m
ayuv                    mpeg1video              sgi
bmp                     mpeg2video              snow
cinepak                 mpeg4                   sonic
cljr                    msmpeg4v2               sonic_ls
comfortnoise            msmpeg4v3               srt
dca                     msvideo1                ssa
dnxhd                   nellymoser              subrip
dpx                     nvenc                   sunrast
dvbsub                  nvenc_h264              svq1
dvdsub                  nvenc_hevc              targa
dvvideo                 pam                     text
eac3                    pbm                     tiff
ffv1                    pcm_alaw                truehd
ffvhuff                 pcm_f32be               tta
flac                    pcm_f32le               utvideo
flashsv                 pcm_f64be               v210
flashsv2                pcm_f64le               v308
flv                     pcm_mulaw               v408
g723_1                  pcm_s16be               v410
gif                     pcm_s16be_planar        vc2
h261                    pcm_s16le               vorbis
h263                    pcm_s16le_planar        wavpack
h263p                   pcm_s24be               webvtt
h264_nvenc              pcm_s24daud             wmav1
hevc_nvenc              pcm_s24le               wmav2
huffyuv                 pcm_s24le_planar        wmv1
jpeg2000                pcm_s32be               wmv2
jpegls                  pcm_s32le               wrapped_avframe
libfdk_aac              pcm_s32le_planar        xbm
libgsm                  pcm_s64be               xface
libgsm_ms               pcm_s64le               xsub
libilbc                 pcm_s8                  xwd
libmp3lame              pcm_s8_planar           y41p
libopencore_amrnb       pcm_u16be               yuv4
libopenjpeg             pcm_u16le               zlib
libopus                 pcm_u24be               zmbv

Enabled hwaccels:

Enabled parsers:
aac                     dvd_nav                 mpegvideo
aac_latm                dvdsub                  opus
ac3                     flac                    png
adx                     g729                    pnm
bmp                     gsm                     rv30
cavsvideo               h261                    rv40
cook                    h263                    tak
dca                     h264                    vc1
dirac                   hevc                    vorbis
dnxhd                   mjpeg                   vp3
dpx                     mlp                     vp8
dvaudio                 mpeg4video              vp9
dvbsub                  mpegaudio

Enabled demuxers:
aa                      flic                    mgsts
aac                     flv                     microdvd
ac3                     fourxm                  mjpeg
acm                     frm                     mlp
act                     fsb                     mlv
adf                     g722                    mm
adp                     g723_1                  mmf
ads                     g729                    mov
adx                     genh                    mp3
aea                     gif                     mpc
afc                     gsm                     mpc8
aiff                    gxf                     mpegps
aix                     h261                    mpegts
amr                     h263                    mpegtsraw
anm                     h264                    mpegvideo
apc                     hevc                    mpjpeg
ape                     hls                     mpl2
apng                    hnm                     mpsub
aqtitle                 ico                     msf
asf                     idcin                   msnwc_tcp
asf_o                   idf                     mtaf
ass                     iff                     mtv
ast                     ilbc                    musx
au                      image2                  mv
avi                     image2_alias_pix        mvi
avr                     image2_brender_pix      mxf
avs                     image2pipe              mxg
bethsoftvid             image_bmp_pipe          nc
bfi                     image_dds_pipe          nistsphere
bfstm                   image_dpx_pipe          nsv
bink                    image_exr_pipe          nut
bintext                 image_j2k_pipe          nuv
bit                     image_jpeg_pipe         ogg
bmv                     image_jpegls_pipe       oma
boa                     image_pam_pipe          paf
brstm                   image_pbm_pipe          pcm_alaw
c93                     image_pcx_pipe          pcm_f32be
caf                     image_pgm_pipe          pcm_f32le
cavsvideo               image_pgmyuv_pipe       pcm_f64be
cdg                     image_pictor_pipe       pcm_f64le
cdxl                    image_png_pipe          pcm_mulaw
cine                    image_ppm_pipe          pcm_s16be
concat                  image_qdraw_pipe        pcm_s16le
data                    image_sgi_pipe          pcm_s24be
daud                    image_sunrast_pipe      pcm_s24le
dcstr                   image_tiff_pipe         pcm_s32be
dfa                     image_webp_pipe         pcm_s32le
dirac                   ingenient               pcm_s8
dnxhd                   ipmovie                 pcm_u16be
dsf                     ircam                   pcm_u16le
dsicin                  iss                     pcm_u24be
dss                     iv8                     pcm_u24le
dts                     ivf                     pcm_u32be
dtshd                   ivr                     pcm_u32le
dv                      jacosub                 pcm_u8
dvbsub                  jv                      pjs
dvbtxt                  libmodplug              pmp
dxa                     libnut                  pva
ea                      live_flv                pvf
ea_cdata                lmlm4                   qcp
eac3                    loas                    r3d
epaf                    lrc                     rawvideo
ffm                     lvf                     realtext
ffmetadata              lxf                     redspark
filmstrip               m4v                     rl2
flac                    matroska                rm
roq                     str                     vobsub
rpl                     subviewer               voc
rsd                     subviewer1              vpk
rso                     sup                     vplayer
rtp                     svag                    vqf
rtsp                    swf                     w64
sami                    tak                     wav
sap                     tedcaptions             wc3
sbg                     thp                     webm_dash_manifest
sdp                     threedostr              webvtt
sdr2                    tiertexseq              wsaud
segafilm                tmv                     wsd
shorten                 truehd                  wsvqa
siff                    tta                     wtv
sln                     tty                     wv
smacker                 txd                     wve
smjpeg                  v210                    xa
smush                   v210x                   xbin
sol                     vag                     xmv
sox                     vc1                     xvag
spdif                   vc1t                    xwma
srt                     vivo                    yop
stl                     vmd                     yuv4mpegpipe

Enabled muxers:
a64                     image2                  pcm_s24be
ac3                     image2pipe              pcm_s24le
adts                    ipod                    pcm_s32be
adx                     ircam                   pcm_s32le
aiff                    ismv                    pcm_s8
amr                     ivf                     pcm_u16be
apng                    jacosub                 pcm_u16le
asf                     latm                    pcm_u24be
asf_stream              libnut                  pcm_u24le
ass                     lrc                     pcm_u32be
ast                     m4v                     pcm_u32le
au                      matroska                pcm_u8
avi                     matroska_audio          psp
avm2                    md5                     rawvideo
bit                     microdvd                rm
caf                     mjpeg                   roq
cavsvideo               mkvtimestamp_v2         rso
crc                     mlp                     rtp
dash                    mmf                     rtp_mpegts
data                    mov                     rtsp
daud                    mp2                     sap
dirac                   mp3                     segment
dnxhd                   mp4                     singlejpeg
dts                     mpeg1system             smjpeg
dv                      mpeg1vcd                smoothstreaming
eac3                    mpeg1video              sox
f4v                     mpeg2dvd                spdif
ffm                     mpeg2svcd               spx
ffmetadata              mpeg2video              srt
fifo                    mpeg2vob                stream_segment
filmstrip               mpegts                  swf
flac                    mpjpeg                  tee
flv                     mxf                     tg2
framecrc                mxf_d10                 tgp
framehash               mxf_opatom              truehd
framemd5                null                    tta
g722                    nut                     uncodedframecrc
g723_1                  oga                     vc1
gif                     ogg                     vc1t
gsm                     ogv                     voc
gxf                     oma                     w64
h261                    opus                    wav
h263                    pcm_alaw                webm
h264                    pcm_f32be               webm_chunk
hash                    pcm_f32le               webm_dash_manifest
hds                     pcm_f64be               webp
hevc                    pcm_f64le               webvtt
hls                     pcm_mulaw               wtv
ico                     pcm_s16be               wv
ilbc                    pcm_s16le               yuv4mpegpipe

Enabled protocols:
async                   http                    mmst
bluray                  httpproxy               pipe
cache                   icecast                 rtp
concat                  librtmp                 srtp
crypto                  librtmpe                subfile
data                    librtmps                tcp
file                    librtmpt                tee
ftp                     librtmpte               udp
gopher                  md5                     udplite
hls                     mmsh                    unix

Enabled filters:
abench                  blackframe              fps
acompressor             blend                   framepack
acrossfade              boxblur                 framerate
acrusher                bs2b                    framestep
adelay                  bwdif                   frei0r
adrawgraph              cellauto                frei0r_src
aecho                   channelmap              fspp
aemphasis               channelsplit            gblur
aeval                   chorus                  geq
aevalsrc                chromakey               gradfun
afade                   ciescope                haldclut
afftfilt                codecview               haldclutsrc
aformat                 color                   hdcd
agate                   colorbalance            hflip
ahistogram              colorchannelmixer       highpass
ainterleave             colorkey                histeq
alimiter                colorlevels             histogram
allpass                 colormatrix             hqdn3d
allrgb                  colorspace              hqx
allyuv                  compand                 hstack
aloop                   compensationdelay       hue
alphaextract            concat                  hwdownload
alphamerge              convolution             hwupload
amerge                  copy                    hysteresis
ametadata               cover_rect              idet
amix                    crop                    il
amovie                  cropdetect              inflate
anequalizer             crystalizer             interlace
anoisesrc               curves                  interleave
anull                   datascope               join
anullsink               dcshift                 kerndeint
anullsrc                dctdnoiz                lenscorrection
apad                    deband                  life
aperms                  decimate                loop
aphasemeter             deflate                 lowpass
aphaser                 dejudder                lut
apulsator               delogo                  lut2
arealtime               deshake                 lut3d
aresample               detelecine              lutrgb
areverse                dilation                lutyuv
aselect                 displace                mandelbrot
asendcmd                drawbox                 maskedclamp
asetnsamples            drawgraph               maskedmerge
asetpts                 drawgrid                mcdeint
asetrate                drawtext                mergeplanes
asettb                  dynaudnorm              mestimate
ashowinfo               earwax                  metadata
asidedata               ebur128                 minterpolate
asplit                  edgedetect              movie
ass                     elbg                    mpdecimate
astats                  eq                      mptestsrc
astreamselect           equalizer               negate
atadenoise              erosion                 nlmeans
atempo                  extractplanes           nnedi
atrim                   extrastereo             noformat
avectorscope            fade                    noise
avgblur                 fftfilt                 null
azmq                    field                   nullsink
bandpass                fieldhint               nullsrc
bandreject              fieldmatch              overlay
bass                    fieldorder              owdenoise
bbox                    find_rect               pad
bench                   firequalizer            palettegen
biquad                  flanger                 paletteuse
bitplanenoise           flite                   pan
blackdetect             format                  perms
perspective             showfreqs               swapuv
phase                   showinfo                tblend
pixdesctest             showpalette             telecine
pp                      showspectrum            testsrc
pp7                     showspectrumpic         testsrc2
prewitt                 showvolume              thumbnail
psnr                    showwaves               tile
pullup                  showwavespic            tinterlace
qp                      shuffleframes           transpose
random                  shuffleplanes           treble
readvitc                sidechaincompress       tremolo
realtime                sidechaingate           trim
remap                   sidedata                unsharp
removegrain             signalstats             uspp
removelogo              silencedetect           vaguedenoiser
repeatfields            silenceremove           vectorscope
replaygain              sine                    vflip
reverse                 smartblur               vibrato
rgbtestsrc              smptebars               vidstabdetect
rotate                  smptehdbars             vidstabtransform
sab                     sobel                   vignette
scale                   spectrumsynth           volume
scale2ref               split                   volumedetect
select                  spp                     vstack
selectivecolor          ssim                    w3fdif
sendcmd                 stereo3d                waveform
separatefields          stereotools             weave
setdar                  stereowiden             xbr
setfield                streamselect            yadif
setpts                  subtitles               yuvtestsrc
setsar                  super2xsai              zmq
settb                   swaprect                zoompan
showcqt

Enabled bsfs:
aac_adtstoasc           imx_dump_header         mpeg4_unpack_bframes
chomp                   mjpeg2jpeg              noise
dca_core                mjpega_dump_header      remove_extradata
dump_extradata          mov2textsub             text2movsub
h264_mp4toannexb        mp3_header_decompress   vp9_superframe
hevc_mp4toannexb

Enabled indevs:
dv1394                  lavfi                   oss
fbdev                   libcdio                 v4l2
iec61883                libdc1394

Enabled outdevs:
caca                    oss                     v4l2
fbdev
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
