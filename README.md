This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more (56) external
libraries included.

Static <b>ffmpeg v4.3.1</b> build from this repository currently compiles on:
<table>
<!-- tr><td><b>CentOS 7.5-1804</b>   </td><td>x86_64</td -->
<tr><td><b>Ubuntu 18.04.1 LTS</b></td><td>amd64</td>
<td rowspan="3">
<img src="http://www.movieconverter-studio.com/_PUBLIC/ffmpeg/logo-new/ffmpeg-logo-src/ffmpeg-logo.png" height="90">
</td></tr>
<!-- tr><td><b>Debian 9.5</b>        </td><td>amd64</td></tr -->
</table>

For build see [BUILD.md].

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            4.3.1
C compiler                gcc
C library                 glibc
big-endian                no
runtime cpu detection     yes
standalone assembly       yes
x86 assembler             nasm
MMX enabled               yes
MMXEXT enabled            yes
3DNow! enabled            yes
3DNow! extended enabled   yes
SSE enabled               yes
SSSE3 enabled             yes
AESNI enabled             yes
AVX enabled               yes
AVX2 enabled              yes
AVX-512 enabled           yes
XOP enabled               yes
FMA3 enabled              yes
FMA4 enabled              yes
i686 features enabled     yes
CMOV is fast              yes
EBX available             yes
EBP available             yes
debug symbols             no
strip symbols             yes
optimize for size         no
optimizations             yes
static                    yes
shared                    no
postprocessing support    yes
network support           yes
threading support         pthreads
safe bitstream reader     yes
texi2html enabled         no
perl enabled              yes
pod2man enabled           yes
makeinfo enabled          no
makeinfo supports HTML    no

External libraries:
avisynth                libkvazaar              libvpx
bzlib                   liblensfun              libwavpack
frei0r                  libmodplug              libwebp
iconv                   libmp3lame              libx264
libaom                  libmysofa               libx265
libass                  libopencore_amrnb       libxavs
libbluray               libopencore_amrwb       libxavs2
libbs2b                 libopencv               libxcb
libcaca                 libopenjpeg             libxcb_shape
libcdio                 libopus                 libxcb_shm
libcodec2               librtmp                 libxcb_xfixes
libdav1d                libshine                libxml2
libdavs2                libsoxr                 libxvid
libdc1394               libspeex                libzimg
libfdk_aac              libtheora               libzmq
libflite                libtwolame              libzvbi
libfontconfig           libv4l2                 lzma
libfreetype             libvidstab              openssl
libgsm                  libvmaf                 xlib
libiec61883             libvo_amrwbenc          zlib
libilbc                 libvorbis

External libraries providing hardware acceleration:
v4l2_m2m

Libraries:
avcodec                 avformat                swresample
avdevice                avutil                  swscale
avfilter                postproc

Programs:
ffmpeg                  ffprobe

Enabled decoders:
aac                     fmvc                    pcm_u24le
aac_fixed               fourxm                  pcm_u32be
aac_latm                fraps                   pcm_u32le
aasc                    frwu                    pcm_u8
ac3                     g2m                     pcm_vidc
ac3_fixed               g723_1                  pcx
acelp_kelvin            g729                    pfm
adpcm_4xm               gdv                     pgm
adpcm_adx               gif                     pgmyuv
adpcm_afc               gremlin_dpcm            pgssub
adpcm_agm               gsm                     pictor
adpcm_aica              gsm_ms                  pixlet
adpcm_argo              h261                    pjs
adpcm_ct                h263                    png
adpcm_dtk               h263_v4l2m2m            ppm
adpcm_ea                h263i                   prores
adpcm_ea_maxis_xa       h263p                   prosumer
adpcm_ea_r1             h264                    psd
adpcm_ea_r2             h264_v4l2m2m            ptx
adpcm_ea_r3             hap                     qcelp
adpcm_ea_xas            hca                     qdm2
adpcm_g722              hcom                    qdmc
adpcm_g726              hevc                    qdraw
adpcm_g726le            hevc_v4l2m2m            qpeg
adpcm_ima_alp           hnm4_video              qtrle
adpcm_ima_amv           hq_hqa                  r10k
adpcm_ima_apc           hqx                     r210
adpcm_ima_apm           huffyuv                 ra_144
adpcm_ima_cunning       hymt                    ra_288
adpcm_ima_dat4          iac                     ralf
adpcm_ima_dk3           idcin                   rasc
adpcm_ima_dk4           idf                     rawvideo
adpcm_ima_ea_eacs       iff_ilbm                realtext
adpcm_ima_ea_sead       ilbc                    rl2
adpcm_ima_iss           imc                     roq
adpcm_ima_mtf           imm4                    roq_dpcm
adpcm_ima_oki           imm5                    rpza
adpcm_ima_qt            indeo2                  rscc
adpcm_ima_rad           indeo3                  rv10
adpcm_ima_smjpeg        indeo4                  rv20
adpcm_ima_ssi           indeo5                  rv30
adpcm_ima_wav           interplay_acm           rv40
adpcm_ima_ws            interplay_dpcm          s302m
adpcm_ms                interplay_video         sami
adpcm_mtaf              jacosub                 sanm
adpcm_psx               jpeg2000                sbc
adpcm_sbpro_2           jpegls                  scpr
adpcm_sbpro_3           jv                      screenpresso
adpcm_sbpro_4           kgv1                    sdx2_dpcm
adpcm_swf               kmvc                    sgi
adpcm_thp               lagarith                sgirle
adpcm_thp_le            libaom_av1              sheervideo
adpcm_vima              libcodec2               shorten
adpcm_xa                libdav1d                sipr
adpcm_yamaha            libdavs2                siren
adpcm_zork              libfdk_aac              smackaud
agm                     libgsm                  smacker
aic                     libgsm_ms               smc
alac                    libilbc                 smvjpeg
alias_pix               libopencore_amrnb       snow
als                     libopencore_amrwb       sol_dpcm
amrnb                   libopenjpeg             sonic
amrwb                   libopus                 sp5x
amv                     libspeex                speedhq
anm                     libvorbis               srgc
ansi                    libvpx_vp8              srt
ape                     libvpx_vp9              ssa
apng                    libzvbi_teletext        stl
aptx                    loco                    subrip
aptx_hd                 lscr                    subviewer
arbc                    m101                    subviewer1
ass                     mace3                   sunrast
asv1                    mace6                   svq1
asv2                    magicyuv                svq3
atrac1                  mdec                    tak
atrac3                  metasound               targa
atrac3al                microdvd                targa_y216
atrac3p                 mimic                   tdsc
atrac3pal               mjpeg                   text
atrac9                  mjpegb                  theora
aura                    mlp                     thp
aura2                   mmvideo                 tiertexseqvideo
avrn                    motionpixels            tiff
avrp                    movtext                 tmv
avs                     mp1                     truehd
avui                    mp1float                truemotion1
ayuv                    mp2                     truemotion2
bethsoftvid             mp2float                truemotion2rt
bfi                     mp3                     truespeech
bink                    mp3adu                  tscc
binkaudio_dct           mp3adufloat             tscc2
binkaudio_rdft          mp3float                tta
bintext                 mp3on4                  twinvq
bitpacked               mp3on4float             txd
bmp                     mpc7                    ulti
bmv_audio               mpc8                    utvideo
bmv_video               mpeg1_v4l2m2m           v210
brender_pix             mpeg1video              v210x
c93                     mpeg2_v4l2m2m           v308
cavs                    mpeg2video              v408
ccaption                mpeg4                   v410
cdgraphics              mpeg4_v4l2m2m           vb
cdtoons                 mpegvideo               vble
cdxl                    mpl2                    vc1
cfhd                    msa1                    vc1_v4l2m2m
cinepak                 mscc                    vc1image
clearvideo              msmpeg4v1               vcr1
cljr                    msmpeg4v2               vmdaudio
cllc                    msmpeg4v3               vmdvideo
comfortnoise            msrle                   vmnc
cook                    mss1                    vorbis
cpia                    mss2                    vp3
cscd                    msvideo1                vp4
cyuv                    mszh                    vp5
dca                     mts2                    vp6
dds                     mv30                    vp6a
derf_dpcm               mvc1                    vp6f
dfa                     mvc2                    vp7
dirac                   mvdv                    vp8
dnxhd                   mvha                    vp8_v4l2m2m
dolby_e                 mwsc                    vp9
dpx                     mxpeg                   vp9_v4l2m2m
dsd_lsbf                nellymoser              vplayer
dsd_lsbf_planar         notchlc                 vqa
dsd_msbf                nuv                     wavpack
dsd_msbf_planar         on2avc                  wcmv
dsicinaudio             opus                    webp
dsicinvideo             paf_audio               webvtt
dss_sp                  paf_video               wmalossless
dst                     pam                     wmapro
dvaudio                 pbm                     wmav1
dvbsub                  pcm_alaw                wmav2
dvdsub                  pcm_bluray              wmavoice
dvvideo                 pcm_dvd                 wmv1
dxa                     pcm_f16le               wmv2
dxtory                  pcm_f24le               wmv3
dxv                     pcm_f32be               wmv3image
eac3                    pcm_f32le               wnv1
eacmv                   pcm_f64be               wrapped_avframe
eamad                   pcm_f64le               ws_snd1
eatgq                   pcm_lxf                 xan_dpcm
eatgv                   pcm_mulaw               xan_wc3
eatqi                   pcm_s16be               xan_wc4
eightbps                pcm_s16be_planar        xbin
eightsvx_exp            pcm_s16le               xbm
eightsvx_fib            pcm_s16le_planar        xface
escape124               pcm_s24be               xl
escape130               pcm_s24daud             xma1
evrc                    pcm_s24le               xma2
exr                     pcm_s24le_planar        xpm
ffv1                    pcm_s32be               xsub
ffvhuff                 pcm_s32le               xwd
ffwavesynth             pcm_s32le_planar        y41p
fic                     pcm_s64be               ylc
fits                    pcm_s64le               yop
flac                    pcm_s8                  yuv4
flashsv                 pcm_s8_planar           zero12v
flashsv2                pcm_u16be               zerocodec
flic                    pcm_u16le               zlib
flv                     pcm_u24be               zmbv

Enabled encoders:
a64multi                libmp3lame              pcm_u24be
a64multi5               libopencore_amrnb       pcm_u24le
aac                     libopenjpeg             pcm_u32be
ac3                     libopus                 pcm_u32le
ac3_fixed               libshine                pcm_u8
adpcm_adx               libspeex                pcm_vidc
adpcm_g722              libtheora               pcx
adpcm_g726              libtwolame              pgm
adpcm_g726le            libvo_amrwbenc          pgmyuv
adpcm_ima_qt            libvorbis               png
adpcm_ima_ssi           libvpx_vp8              ppm
adpcm_ima_wav           libvpx_vp9              prores
adpcm_ms                libwavpack              prores_aw
adpcm_swf               libwebp                 prores_ks
adpcm_yamaha            libwebp_anim            qtrle
alac                    libx264                 r10k
alias_pix               libx264rgb              r210
amv                     libx265                 ra_144
apng                    libxavs                 rawvideo
aptx                    libxavs2                roq
aptx_hd                 libxvid                 roq_dpcm
ass                     ljpeg                   rv10
asv1                    magicyuv                rv20
asv2                    mjpeg                   s302m
avrp                    mlp                     sbc
avui                    movtext                 sgi
ayuv                    mp2                     snow
bmp                     mp2fixed                sonic
cinepak                 mpeg1video              sonic_ls
cljr                    mpeg2video              srt
comfortnoise            mpeg4                   ssa
dca                     mpeg4_v4l2m2m           subrip
dnxhd                   msmpeg4v2               sunrast
dpx                     msmpeg4v3               svq1
dvbsub                  msvideo1                targa
dvdsub                  nellymoser              text
dvvideo                 opus                    tiff
eac3                    pam                     truehd
ffv1                    pbm                     tta
ffvhuff                 pcm_alaw                utvideo
fits                    pcm_dvd                 v210
flac                    pcm_f32be               v308
flashsv                 pcm_f32le               v408
flashsv2                pcm_f64be               v410
flv                     pcm_f64le               vc2
g723_1                  pcm_mulaw               vorbis
gif                     pcm_s16be               vp8_v4l2m2m
h261                    pcm_s16be_planar        wavpack
h263                    pcm_s16le               webvtt
h263_v4l2m2m            pcm_s16le_planar        wmav1
h263p                   pcm_s24be               wmav2
h264_v4l2m2m            pcm_s24daud             wmv1
hevc_v4l2m2m            pcm_s24le               wmv2
huffyuv                 pcm_s24le_planar        wrapped_avframe
jpeg2000                pcm_s32be               xbm
jpegls                  pcm_s32le               xface
libaom_av1              pcm_s32le_planar        xsub
libcodec2               pcm_s64be               xwd
libfdk_aac              pcm_s64le               y41p
libgsm                  pcm_s8                  yuv4
libgsm_ms               pcm_s8_planar           zlib
libilbc                 pcm_u16be               zmbv
libkvazaar              pcm_u16le

Enabled hwaccels:

Enabled parsers:
aac                     dvdsub                  opus
aac_latm                flac                    png
ac3                     g723_1                  pnm
adx                     g729                    rv30
av1                     gif                     rv40
avs2                    gsm                     sbc
bmp                     h261                    sipr
cavsvideo               h263                    tak
cook                    h264                    vc1
dca                     hevc                    vorbis
dirac                   jpeg2000                vp3
dnxhd                   mjpeg                   vp8
dpx                     mlp                     vp9
dvaudio                 mpeg4video              webp
dvbsub                  mpegaudio               xma
dvd_nav                 mpegvideo

Enabled demuxers:
aa                      hls                     pcm_s24le
aac                     hnm                     pcm_s32be
ac3                     ico                     pcm_s32le
acm                     idcin                   pcm_s8
act                     idf                     pcm_u16be
adf                     iff                     pcm_u16le
adp                     ifv                     pcm_u24be
ads                     ilbc                    pcm_u24le
adx                     image2                  pcm_u32be
aea                     image2_alias_pix        pcm_u32le
afc                     image2_brender_pix      pcm_u8
aiff                    image2pipe              pcm_vidc
aix                     image_bmp_pipe          pjs
alp                     image_dds_pipe          pmp
amr                     image_dpx_pipe          pp_bnk
amrnb                   image_exr_pipe          pva
amrwb                   image_gif_pipe          pvf
anm                     image_j2k_pipe          qcp
apc                     image_jpeg_pipe         r3d
ape                     image_jpegls_pipe       rawvideo
apm                     image_pam_pipe          realtext
apng                    image_pbm_pipe          redspark
aptx                    image_pcx_pipe          rl2
aptx_hd                 image_pgm_pipe          rm
aqtitle                 image_pgmyuv_pipe       roq
argo_asf                image_pictor_pipe       rpl
asf                     image_png_pipe          rsd
asf_o                   image_ppm_pipe          rso
ass                     image_psd_pipe          rtp
ast                     image_qdraw_pipe        rtsp
au                      image_sgi_pipe          s337m
av1                     image_sunrast_pipe      sami
avi                     image_svg_pipe          sap
avisynth                image_tiff_pipe         sbc
avr                     image_webp_pipe         sbg
avs                     image_xpm_pipe          scc
avs2                    image_xwd_pipe          sdp
bethsoftvid             ingenient               sdr2
bfi                     ipmovie                 sds
bfstm                   ircam                   sdx
bink                    iss                     segafilm
bintext                 iv8                     ser
bit                     ivf                     shorten
bmv                     ivr                     siff
boa                     jacosub                 sln
brstm                   jv                      smacker
c93                     kux                     smjpeg
caf                     kvag                    smush
cavsvideo               libmodplug              sol
cdg                     live_flv                sox
cdxl                    lmlm4                   spdif
cine                    loas                    srt
codec2                  lrc                     stl
codec2raw               lvf                     str
concat                  lxf                     subviewer
dash                    m4v                     subviewer1
data                    matroska                sup
daud                    mgsts                   svag
dcstr                   microdvd                swf
derf                    mjpeg                   tak
dfa                     mjpeg_2000              tedcaptions
dhav                    mlp                     thp
dirac                   mlv                     threedostr
dnxhd                   mm                      tiertexseq
dsf                     mmf                     tmv
dsicin                  mov                     truehd
dss                     mp3                     tta
dts                     mpc                     tty
dtshd                   mpc8                    txd
dv                      mpegps                  ty
dvbsub                  mpegts                  v210
dvbtxt                  mpegtsraw               v210x
dxa                     mpegvideo               vag
ea                      mpjpeg                  vc1
ea_cdata                mpl2                    vc1t
eac3                    mpsub                   vividas
epaf                    msf                     vivo
ffmetadata              msnwc_tcp               vmd
filmstrip               mtaf                    vobsub
fits                    mtv                     voc
flac                    musx                    vpk
flic                    mv                      vplayer
flv                     mvi                     vqf
fourxm                  mxf                     w64
frm                     mxg                     wav
fsb                     nc                      wc3
fwse                    nistsphere              webm_dash_manifest
g722                    nsp                     webvtt
g723_1                  nsv                     wsaud
g726                    nut                     wsd
g726le                  nuv                     wsvqa
g729                    ogg                     wtv
gdv                     oma                     wv
genh                    paf                     wve
gif                     pcm_alaw                xa
gsm                     pcm_f32be               xbin
gxf                     pcm_f32le               xmv
h261                    pcm_f64be               xvag
h263                    pcm_f64le               xwma
h264                    pcm_mulaw               yop
hca                     pcm_s16be               yuv4mpegpipe
hcom                    pcm_s16le
hevc                    pcm_s24be

Enabled muxers:
a64                     hls                     pcm_s32be
ac3                     ico                     pcm_s32le
adts                    ilbc                    pcm_s8
adx                     image2                  pcm_u16be
aiff                    image2pipe              pcm_u16le
amr                     ipod                    pcm_u24be
apng                    ircam                   pcm_u24le
aptx                    ismv                    pcm_u32be
aptx_hd                 ivf                     pcm_u32le
asf                     jacosub                 pcm_u8
asf_stream              kvag                    pcm_vidc
ass                     latm                    psp
ast                     lrc                     rawvideo
au                      m4v                     rm
avi                     matroska                roq
avm2                    matroska_audio          rso
avs2                    md5                     rtp
bit                     microdvd                rtp_mpegts
caf                     mjpeg                   rtsp
cavsvideo               mkvtimestamp_v2         sap
codec2                  mlp                     sbc
codec2raw               mmf                     scc
crc                     mov                     segafilm
dash                    mp2                     segment
data                    mp3                     singlejpeg
daud                    mp4                     smjpeg
dirac                   mpeg1system             smoothstreaming
dnxhd                   mpeg1vcd                sox
dts                     mpeg1video              spdif
dv                      mpeg2dvd                spx
eac3                    mpeg2svcd               srt
f4v                     mpeg2video              stream_segment
ffmetadata              mpeg2vob                streamhash
fifo                    mpegts                  sup
fifo_test               mpjpeg                  swf
filmstrip               mxf                     tee
fits                    mxf_d10                 tg2
flac                    mxf_opatom              tgp
flv                     null                    truehd
framecrc                nut                     tta
framehash               oga                     uncodedframecrc
framemd5                ogg                     vc1
g722                    ogv                     vc1t
g723_1                  oma                     voc
g726                    opus                    w64
g726le                  pcm_alaw                wav
gif                     pcm_f32be               webm
gsm                     pcm_f32le               webm_chunk
gxf                     pcm_f64be               webm_dash_manifest
h261                    pcm_f64le               webp
h263                    pcm_mulaw               webvtt
h264                    pcm_s16be               wtv
hash                    pcm_s16le               wv
hds                     pcm_s24be               yuv4mpegpipe
hevc                    pcm_s24le

Enabled protocols:
async                   https                   prompeg
bluray                  icecast                 rtp
cache                   librtmp                 srtp
concat                  librtmpe                subfile
crypto                  librtmps                tcp
data                    librtmpt                tee
file                    librtmpte               tls
ftp                     libzmq                  udp
gopher                  md5                     udplite
hls                     mmsh                    unix
http                    mmst
httpproxy               pipe

Enabled filters:
abench                  deflate                 pan
abitscope               deflicker               perms
acompressor             dejudder                perspective
acontrast               delogo                  phase
acopy                   derain                  photosensitivity
acrossfade              deshake                 pixdesctest
acrossover              despill                 pixscope
acrusher                detelecine              pp
acue                    dilation                pp7
addroi                  displace                premultiply
adeclick                dnn_processing          prewitt
adeclip                 doubleweave             pseudocolor
adelay                  drawbox                 psnr
aderivative             drawgraph               pullup
adrawgraph              drawgrid                qp
aecho                   drawtext                random
aemphasis               drmeter                 readeia608
aeval                   dynaudnorm              readvitc
aevalsrc                earwax                  realtime
afade                   ebur128                 remap
afftdn                  edgedetect              removegrain
afftfilt                elbg                    removelogo
afifo                   entropy                 repeatfields
afir                    eq                      replaygain
afirsrc                 equalizer               reverse
aformat                 erosion                 rgbashift
agate                   extractplanes           rgbtestsrc
agraphmonitor           extrastereo             roberts
ahistogram              fade                    rotate
aiir                    fftdnoiz                sab
aintegral               fftfilt                 scale
ainterleave             field                   scale2ref
alimiter                fieldhint               scdet
allpass                 fieldmatch              scroll
allrgb                  fieldorder              select
allyuv                  fifo                    selectivecolor
aloop                   fillborders             sendcmd
alphaextract            find_rect               separatefields
alphamerge              firequalizer            setdar
amerge                  flanger                 setfield
ametadata               flite                   setparams
amix                    floodfill               setpts
amovie                  format                  setrange
amplify                 fps                     setsar
amultiply               framepack               settb
anequalizer             framerate               showcqt
anlmdn                  framestep               showfreqs
anlms                   freezedetect            showinfo
anoisesrc               freezeframes            showpalette
anull                   frei0r                  showspatial
anullsink               frei0r_src              showspectrum
anullsrc                fspp                    showspectrumpic
apad                    gblur                   showvolume
aperms                  geq                     showwaves
aphasemeter             gradfun                 showwavespic
aphaser                 gradients               shuffleframes
apulsator               graphmonitor            shuffleplanes
arealtime               greyedge                sidechaincompress
aresample               haas                    sidechaingate
areverse                haldclut                sidedata
arnndn                  haldclutsrc             sierpinski
aselect                 hdcd                    signalstats
asendcmd                headphone               signature
asetnsamples            hflip                   silencedetect
asetpts                 highpass                silenceremove
asetrate                highshelf               sinc
asettb                  hilbert                 sine
ashowinfo               histeq                  smartblur
asidedata               histogram               smptebars
asoftclip               hqdn3d                  smptehdbars
asplit                  hqx                     sobel
ass                     hstack                  sofalizer
astats                  hue                     spectrumsynth
astreamselect           hwdownload              split
asubboost               hwmap                   spp
atadenoise              hwupload                sr
atempo                  hysteresis              ssim
atrim                   idet                    stereo3d
avectorscope            il                      stereotools
avgblur                 inflate                 stereowiden
axcorrelate             interlace               streamselect
azmq                    interleave              subtitles
bandpass                join                    super2xsai
bandreject              kerndeint               superequalizer
bass                    lagfun                  surround
bbox                    lenscorrection          swaprect
bench                   lensfun                 swapuv
bilateral               libvmaf                 tblend
biquad                  life                    telecine
bitplanenoise           limiter                 testsrc
blackdetect             loop                    testsrc2
blackframe              loudnorm                thistogram
blend                   lowpass                 threshold
bm3d                    lowshelf                thumbnail
boxblur                 lumakey                 tile
bs2b                    lut                     tinterlace
bwdif                   lut1d                   tlut2
cas                     lut2                    tmedian
cellauto                lut3d                   tmix
channelmap              lutrgb                  tonemap
channelsplit            lutyuv                  tpad
chorus                  mandelbrot              transpose
chromahold              maskedclamp             treble
chromakey               maskedmax               tremolo
chromashift             maskedmerge             trim
ciescope                maskedmin               unpremultiply
codecview               maskedthreshold         unsharp
color                   maskfun                 untile
colorbalance            mcdeint                 uspp
colorchannelmixer       mcompand                v360
colorhold               median                  vaguedenoiser
colorkey                mergeplanes             vectorscope
colorlevels             mestimate               vflip
colormatrix             metadata                vfrdet
colorspace              midequalizer            vibrance
compand                 minterpolate            vibrato
compensationdelay       mix                     vidstabdetect
concat                  movie                   vidstabtransform
convolution             mpdecimate              vignette
convolve                mptestsrc               vmafmotion
copy                    negate                  volume
cover_rect              nlmeans                 volumedetect
crop                    nnedi                   vstack
cropdetect              noformat                w3fdif
crossfeed               noise                   waveform
crystalizer             normalize               weave
cue                     null                    xbr
curves                  nullsink                xfade
datascope               nullsrc                 xmedian
dblur                   ocv                     xstack
dcshift                 oscilloscope            yadif
dctdnoiz                overlay                 yaepblur
deband                  owdenoise               yuvtestsrc
deblock                 pad                     zmq
decimate                pal100bars              zoompan
deconvolve              pal75bars               zscale
dedot                   palettegen
deesser                 paletteuse

Enabled bsfs:
aac_adtstoasc           h264_redundant_pps      null
av1_frame_merge         hapqa_extract           opus_metadata
av1_frame_split         hevc_metadata           pcm_rechunk
av1_metadata            hevc_mp4toannexb        prores_metadata
chomp                   imx_dump_header         remove_extradata
dca_core                mjpeg2jpeg              text2movsub
dump_extradata          mjpega_dump_header      trace_headers
eac3_core               mov2textsub             truehd_core
extract_extradata       mp3_header_decompress   vp9_metadata
filter_units            mpeg2_metadata          vp9_raw_reorder
h264_metadata           mpeg4_unpack_bframes    vp9_superframe
h264_mp4toannexb        noise                   vp9_superframe_split

Enabled indevs:
fbdev                   libcdio                 v4l2
iec61883                libdc1394               xcbgrab
lavfi                   oss

Enabled outdevs:
caca                    oss                     xv
fbdev                   v4l2
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
