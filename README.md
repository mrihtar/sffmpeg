This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more (56) external
libraries included.

Static <b>ffmpeg v4.0.2</b> build from this repository currently compiles on:
<table>
<tr><td><b><!-- CentOS 7.5-1804 --></b>   </td><td><!-- x86_64 --></td>
<td rowspan="3">
<img src="http://www.movieconverter-studio.com/_PUBLIC/ffmpeg/logo-new/ffmpeg-logo-src/ffmpeg-logo.png" height="90">
</td></tr>
<tr><td><b>Ubuntu 18.04.1 LTS</b></td><td>amd64</td></tr>
<tr><td><b><!-- Debian 9.5 --></b>        </td><td><!-- amd64 --></td></tr>
</table>

For build see [BUILD.md].

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            4.0.2
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
bzlib			libmodplug		libvpx
frei0r			libmp3lame		libwavpack
iconv			libopencore_amrnb	libwebp
libass			libopencore_amrwb	libx264
libbluray		libopenjpeg		libx265
libbs2b			libopus			libxavs
libcaca			librtmp			libxcb
libcdio			libshine		libxcb_shape
libdc1394		libsoxr			libxcb_shm
libfdk_aac		libspeex		libxcb_xfixes
libflite		libtheora		libxvid
libfontconfig		libtwolame		libzmq
libfreetype		libv4l2			libzvbi
libgsm			libvidstab		lzma
libiec61883		libvo_amrwbenc		xlib
libilbc			libvorbis		zlib

External libraries providing hardware acceleration:
v4l2_m2m

Libraries:
avcodec			avformat		swresample
avdevice		avutil			swscale
avfilter		postproc

Programs:
ffmpeg			ffprobe

Enabled decoders:
aac			atrac3p			escape124
aac_fixed		atrac3pal		escape130
aac_latm		aura			evrc
aasc			aura2			exr
ac3			avrn			ffv1
ac3_fixed		avrp			ffvhuff
adpcm_4xm		avs			ffwavesynth
adpcm_adx		avui			fic
adpcm_afc		ayuv			fits
adpcm_aica		bethsoftvid		flac
adpcm_ct		bfi			flashsv
adpcm_dtk		bink			flashsv2
adpcm_ea		binkaudio_dct		flic
adpcm_ea_maxis_xa	binkaudio_rdft		flv
adpcm_ea_r1		bintext			fmvc
adpcm_ea_r2		bitpacked		fourxm
adpcm_ea_r3		bmp			fraps
adpcm_ea_xas		bmv_audio		frwu
adpcm_g722		bmv_video		g2m
adpcm_g726		brender_pix		g723_1
adpcm_g726le		c93			g729
adpcm_ima_amv		cavs			gdv
adpcm_ima_apc		ccaption		gif
adpcm_ima_dat4		cdgraphics		gremlin_dpcm
adpcm_ima_dk3		cdxl			gsm
adpcm_ima_dk4		cfhd			gsm_ms
adpcm_ima_ea_eacs	cinepak			h261
adpcm_ima_ea_sead	clearvideo		h263
adpcm_ima_iss		cljr			h263_v4l2m2m
adpcm_ima_oki		cllc			h263i
adpcm_ima_qt		comfortnoise		h263p
adpcm_ima_rad		cook			h264
adpcm_ima_smjpeg	cpia			h264_v4l2m2m
adpcm_ima_wav		cscd			hap
adpcm_ima_ws		cyuv			hevc
adpcm_ms		dca			hnm4_video
adpcm_mtaf		dds			hq_hqa
adpcm_psx		dfa			hqx
adpcm_sbpro_2		dirac			huffyuv
adpcm_sbpro_3		dnxhd			iac
adpcm_sbpro_4		dolby_e			idcin
adpcm_swf		dpx			idf
adpcm_thp		dsd_lsbf		iff_ilbm
adpcm_thp_le		dsd_lsbf_planar		imc
adpcm_vima		dsd_msbf		indeo2
adpcm_xa		dsd_msbf_planar		indeo3
adpcm_yamaha		dsicinaudio		indeo4
aic			dsicinvideo		indeo5
alac			dss_sp			interplay_acm
alias_pix		dst			interplay_dpcm
als			dvaudio			interplay_video
amrnb			dvbsub			jacosub
amrwb			dvdsub			jpeg2000
amv			dvvideo			jpegls
anm			dxa			jv
ansi			dxtory			kgv1
ape			dxv			kmvc
apng			eac3			lagarith
aptx			eacmv			libfdk_aac
aptx_hd			eamad			libgsm
ass			eatgq			libgsm_ms
asv1			eatgv			libilbc
asv2			eatqi			libopencore_amrnb
atrac1			eightbps		libopencore_amrwb
atrac3			eightsvx_exp		libopenjpeg
atrac3al		eightsvx_fib		libopus
libspeex		pcm_f24le		sami
libvorbis		pcm_f32be		sanm
libvpx_vp8		pcm_f32le		sbc
libvpx_vp9		pcm_f64be		scpr
libzvbi_teletext	pcm_f64le		screenpresso
loco			pcm_lxf			sdx2_dpcm
m101			pcm_mulaw		sgi
mace3			pcm_s16be		sgirle
mace6			pcm_s16be_planar	sheervideo
magicyuv		pcm_s16le		shorten
mdec			pcm_s16le_planar	sipr
metasound		pcm_s24be		smackaud
microdvd		pcm_s24daud		smacker
mimic			pcm_s24le		smc
mjpeg			pcm_s24le_planar	smvjpeg
mjpegb			pcm_s32be		snow
mlp			pcm_s32le		sol_dpcm
mmvideo			pcm_s32le_planar	sonic
motionpixels		pcm_s64be		sp5x
movtext			pcm_s64le		speedhq
mp1			pcm_s8			srgc
mp1float		pcm_s8_planar		srt
mp2			pcm_u16be		ssa
mp2float		pcm_u16le		stl
mp3			pcm_u24be		subrip
mp3adu			pcm_u24le		subviewer
mp3adufloat		pcm_u32be		subviewer1
mp3float		pcm_u32le		sunrast
mp3on4			pcm_u8			svq1
mp3on4float		pcm_zork		svq3
mpc7			pcx			tak
mpc8			pgm			targa
mpeg1_v4l2m2m		pgmyuv			targa_y216
mpeg1video		pgssub			tdsc
mpeg2_v4l2m2m		pictor			text
mpeg2video		pixlet			theora
mpeg4			pjs			thp
mpeg4_v4l2m2m		png			tiertexseqvideo
mpegvideo		ppm			tiff
mpl2			prores			tmv
msa1			prores_lgpl		truehd
mscc			psd			truemotion1
msmpeg4v1		ptx			truemotion2
msmpeg4v2		qcelp			truemotion2rt
msmpeg4v3		qdm2			truespeech
msrle			qdmc			tscc
mss1			qdraw			tscc2
mss2			qpeg			tta
msvideo1		qtrle			twinvq
mszh			r10k			txd
mts2			r210			ulti
mvc1			ra_144			utvideo
mvc2			ra_288			v210
mxpeg			ralf			v210x
nellymoser		rawvideo		v308
nuv			realtext		v408
on2avc			rl2			v410
opus			roq			vb
paf_audio		roq_dpcm		vble
paf_video		rpza			vc1
pam			rscc			vc1_v4l2m2m
pbm			rv10			vc1image
pcm_alaw		rv20			vcr1
pcm_bluray		rv30			vmdaudio
pcm_dvd			rv40			vmdvideo
pcm_f16le		s302m			vmnc
vorbis			wmalossless		xbm
vp3			wmapro			xface
vp5			wmav1			xl
vp6			wmav2			xma1
vp6a			wmavoice		xma2
vp6f			wmv1			xpm
vp7			wmv2			xsub
vp8			wmv3			xwd
vp8_v4l2m2m		wmv3image		y41p
vp9			wnv1			ylc
vp9_v4l2m2m		wrapped_avframe		yop
vplayer			ws_snd1			yuv4
vqa			xan_dpcm		zero12v
wavpack			xan_wc3			zerocodec
webp			xan_wc4			zlib
webvtt			xbin			zmbv

Enabled encoders:
a64multi		libopenjpeg		pcm_u24le
a64multi5		libopus			pcm_u32be
aac			libshine		pcm_u32le
ac3			libspeex		pcm_u8
ac3_fixed		libtheora		pcx
adpcm_adx		libtwolame		pgm
adpcm_g722		libvo_amrwbenc		pgmyuv
adpcm_g726		libvorbis		png
adpcm_g726le		libvpx_vp8		ppm
adpcm_ima_qt		libvpx_vp9		prores
adpcm_ima_wav		libwavpack		prores_aw
adpcm_ms		libwebp			prores_ks
adpcm_swf		libwebp_anim		qtrle
adpcm_yamaha		libx264			r10k
alac			libx264rgb		r210
alias_pix		libx265			ra_144
amv			libxavs			rawvideo
apng			libxvid			roq
aptx			ljpeg			roq_dpcm
aptx_hd			magicyuv		rv10
ass			mjpeg			rv20
asv1			mlp			s302m
asv2			movtext			sbc
avrp			mp2			sgi
avui			mp2fixed		snow
ayuv			mpeg1video		sonic
bmp			mpeg2video		sonic_ls
cinepak			mpeg4			srt
cljr			mpeg4_v4l2m2m		ssa
comfortnoise		msmpeg4v2		subrip
dca			msmpeg4v3		sunrast
dnxhd			msvideo1		svq1
dpx			nellymoser		targa
dvbsub			opus			text
dvdsub			pam			tiff
dvvideo			pbm			truehd
eac3			pcm_alaw		tta
ffv1			pcm_f32be		utvideo
ffvhuff			pcm_f32le		v210
fits			pcm_f64be		v308
flac			pcm_f64le		v408
flashsv			pcm_mulaw		v410
flashsv2		pcm_s16be		vc2
flv			pcm_s16be_planar	vorbis
g723_1			pcm_s16le		vp8_v4l2m2m
gif			pcm_s16le_planar	wavpack
h261			pcm_s24be		webvtt
h263			pcm_s24daud		wmav1
h263_v4l2m2m		pcm_s24le		wmav2
h263p			pcm_s24le_planar	wmv1
h264_v4l2m2m		pcm_s32be		wmv2
huffyuv			pcm_s32le		wrapped_avframe
jpeg2000		pcm_s32le_planar	xbm
jpegls			pcm_s64be		xface
libfdk_aac		pcm_s64le		xsub
libgsm			pcm_s8			xwd
libgsm_ms		pcm_s8_planar		y41p
libilbc			pcm_u16be		yuv4
libmp3lame		pcm_u16le		zlib
libopencore_amrnb	pcm_u24be		zmbv

Enabled hwaccels:

Enabled parsers:
aac			dvdsub			png
aac_latm		flac			pnm
ac3			g729			rv30
adx			gsm			rv40
bmp			h261			sbc
cavsvideo		h263			sipr
cook			h264			tak
dca			hevc			vc1
dirac			mjpeg			vorbis
dnxhd			mlp			vp3
dpx			mpeg4video		vp8
dvaudio			mpegaudio		vp9
dvbsub			mpegvideo		xma
dvd_nav			opus

Enabled demuxers:
aa			eac3			jacosub
aac			epaf			jv
ac3			ffmetadata		libmodplug
acm			filmstrip		live_flv
act			fits			lmlm4
adf			flac			loas
adp			flic			lrc
ads			flv			lvf
adx			fourxm			lxf
aea			frm			m4v
afc			fsb			matroska
aiff			g722			mgsts
aix			g723_1			microdvd
amr			g726			mjpeg
amrnb			g726le			mjpeg_2000
amrwb			g729			mlp
anm			gdv			mlv
apc			genh			mm
ape			gif			mmf
apng			gsm			mov
aptx			gxf			mp3
aptx_hd			h261			mpc
aqtitle			h263			mpc8
asf			h264			mpegps
asf_o			hevc			mpegts
ass			hls			mpegtsraw
ast			hnm			mpegvideo
au			ico			mpjpeg
avi			idcin			mpl2
avr			idf			mpsub
avs			iff			msf
bethsoftvid		ilbc			msnwc_tcp
bfi			image2			mtaf
bfstm			image2_alias_pix	mtv
bink			image2_brender_pix	musx
bintext			image2pipe		mv
bit			image_bmp_pipe		mvi
bmv			image_dds_pipe		mxf
boa			image_dpx_pipe		mxg
brstm			image_exr_pipe		nc
c93			image_j2k_pipe		nistsphere
caf			image_jpeg_pipe		nsp
cavsvideo		image_jpegls_pipe	nsv
cdg			image_pam_pipe		nut
cdxl			image_pbm_pipe		nuv
cine			image_pcx_pipe		ogg
codec2			image_pgm_pipe		oma
codec2raw		image_pgmyuv_pipe	paf
concat			image_pictor_pipe	pcm_alaw
data			image_png_pipe		pcm_f32be
daud			image_ppm_pipe		pcm_f32le
dcstr			image_psd_pipe		pcm_f64be
dfa			image_qdraw_pipe	pcm_f64le
dirac			image_sgi_pipe		pcm_mulaw
dnxhd			image_sunrast_pipe	pcm_s16be
dsf			image_svg_pipe		pcm_s16le
dsicin			image_tiff_pipe		pcm_s24be
dss			image_webp_pipe		pcm_s24le
dts			image_xpm_pipe		pcm_s32be
dtshd			ingenient		pcm_s32le
dv			ipmovie			pcm_s8
dvbsub			ircam			pcm_u16be
dvbtxt			iss			pcm_u16le
dxa			iv8			pcm_u24be
ea			ivf			pcm_u24le
ea_cdata		ivr			pcm_u32be
pcm_u32le		shorten			v210x
pcm_u8			siff			vag
pjs			sln			vc1
pmp			smacker			vc1t
pva			smjpeg			vivo
pvf			smush			vmd
qcp			sol			vobsub
r3d			sox			voc
rawvideo		spdif			vpk
realtext		srt			vplayer
redspark		stl			vqf
rl2			str			w64
rm			subviewer		wav
roq			subviewer1		wc3
rpl			sup			webm_dash_manifest
rsd			svag			webvtt
rso			swf			wsaud
rtp			tak			wsd
rtsp			tedcaptions		wsvqa
s337m			thp			wtv
sami			threedostr		wv
sap			tiertexseq		wve
sbc			tmv			xa
sbg			truehd			xbin
scc			tta			xmv
sdp			tty			xvag
sdr2			txd			xwma
sds			ty			yop
sdx			v210			yuv4mpegpipe
segafilm

Enabled muxers:
a64			hls			pcm_s24le
ac3			ico			pcm_s32be
adts			ilbc			pcm_s32le
adx			image2			pcm_s8
aiff			image2pipe		pcm_u16be
amr			ipod			pcm_u16le
apng			ircam			pcm_u24be
aptx			ismv			pcm_u24le
aptx_hd			ivf			pcm_u32be
asf			jacosub			pcm_u32le
asf_stream		latm			pcm_u8
ass			lrc			psp
ast			m4v			rawvideo
au			matroska		rm
avi			matroska_audio		roq
avm2			md5			rso
bit			microdvd		rtp
caf			mjpeg			rtp_mpegts
cavsvideo		mkvtimestamp_v2		rtsp
codec2			mlp			sap
codec2raw		mmf			sbc
crc			mov			scc
dash			mp2			segafilm
data			mp3			segment
daud			mp4			singlejpeg
dirac			mpeg1system		smjpeg
dnxhd			mpeg1vcd		smoothstreaming
dts			mpeg1video		sox
dv			mpeg2dvd		spdif
eac3			mpeg2svcd		spx
f4v			mpeg2video		srt
ffmetadata		mpeg2vob		stream_segment
fifo			mpegts			sup
fifo_test		mpjpeg			swf
filmstrip		mxf			tee
fits			mxf_d10			tg2
flac			mxf_opatom		tgp
flv			null			truehd
framecrc		nut			tta
framehash		oga			uncodedframecrc
framemd5		ogg			vc1
g722			ogv			vc1t
g723_1			oma			voc
g726			opus			w64
g726le			pcm_alaw		wav
gif			pcm_f32be		webm
gsm			pcm_f32le		webm_chunk
gxf			pcm_f64be		webm_dash_manifest
h261			pcm_f64le		webp
h263			pcm_mulaw		webvtt
h264			pcm_s16be		wtv
hash			pcm_s16le		wv
hds			pcm_s24be		yuv4mpegpipe
hevc

Enabled protocols:
async			httpproxy		pipe
bluray			icecast			prompeg
cache			librtmp			rtp
concat			librtmpe		srtp
crypto			librtmps		subfile
data			librtmpt		tcp
file			librtmpte		tee
ftp			md5			udp
gopher			mmsh			udplite
hls			mmst			unix
http

Enabled filters:
abench			bass			erosion
abitscope		bbox			extractplanes
acompressor		bench			extrastereo
acontrast		biquad			fade
acopy			bitplanenoise		fftfilt
acrossfade		blackdetect		field
acrusher		blackframe		fieldhint
adelay			blend			fieldmatch
adrawgraph		boxblur			fieldorder
aecho			bs2b			fifo
aemphasis		bwdif			fillborders
aeval			cellauto		find_rect
aevalsrc		channelmap		firequalizer
afade			channelsplit		flanger
afftfilt		chorus			flite
afifo			chromakey		floodfill
afir			ciescope		format
aformat			codecview		fps
agate			color			framepack
ahistogram		colorbalance		framerate
aiir			colorchannelmixer	framestep
ainterleave		colorkey		frei0r
alimiter		colorlevels		frei0r_src
allpass			colormatrix		fspp
allrgb			colorspace		gblur
allyuv			compand			geq
aloop			compensationdelay	gradfun
alphaextract		concat			haas
alphamerge		convolution		haldclut
amerge			convolve		haldclutsrc
ametadata		copy			hdcd
amix			cover_rect		headphone
amovie			crop			hflip
anequalizer		cropdetect		highpass
anoisesrc		crossfeed		hilbert
anull			crystalizer		histeq
anullsink		curves			histogram
anullsrc		datascope		hqdn3d
apad			dcshift			hqx
aperms			dctdnoiz		hstack
aphasemeter		deband			hue
aphaser			decimate		hwdownload
apulsator		deconvolve		hwmap
arealtime		deflate			hwupload
aresample		deflicker		hysteresis
areverse		dejudder		idet
aselect			delogo			il
asendcmd		deshake			inflate
asetnsamples		despill			interlace
asetpts			detelecine		interleave
asetrate		dilation		join
asettb			displace		kerndeint
ashowinfo		doubleweave		lenscorrection
asidedata		drawbox			life
asplit			drawgraph		limiter
ass			drawgrid		loop
astats			drawtext		loudnorm
astreamselect		drmeter			lowpass
atadenoise		dynaudnorm		lumakey
atempo			earwax			lut
atrim			ebur128			lut2
avectorscope		edgedetect		lut3d
avgblur			elbg			lutrgb
azmq			entropy			lutyuv
bandpass		eq			mandelbrot
bandreject		equalizer		maskedclamp
maskedmerge		removelogo		stereo3d
mcdeint			repeatfields		stereotools
mcompand		replaygain		stereowiden
mergeplanes		reverse			streamselect
mestimate		rgbtestsrc		subtitles
metadata		roberts			super2xsai
midequalizer		rotate			superequalizer
minterpolate		sab			surround
mix			scale			swaprect
movie			scale2ref		swapuv
mpdecimate		select			tblend
mptestsrc		selectivecolor		telecine
negate			sendcmd			testsrc
nlmeans			separatefields		testsrc2
nnedi			setdar			threshold
noformat		setfield		thumbnail
noise			setpts			tile
normalize		setrange		tinterlace
null			setsar			tlut2
nullsink		settb			tonemap
nullsrc			showcqt			transpose
oscilloscope		showfreqs		treble
overlay			showinfo		tremolo
owdenoise		showpalette		trim
pad			showspectrum		unpremultiply
palettegen		showspectrumpic		unsharp
paletteuse		showvolume		uspp
pan			showwaves		vaguedenoiser
perms			showwavespic		vectorscope
perspective		shuffleframes		vflip
phase			shuffleplanes		vfrdet
pixdesctest		sidechaincompress	vibrato
pixscope		sidechaingate		vidstabdetect
pp			sidedata		vidstabtransform
pp7			signalstats		vignette
premultiply		signature		vmafmotion
prewitt			silencedetect		volume
pseudocolor		silenceremove		volumedetect
psnr			sine			vstack
pullup			smartblur		w3fdif
qp			smptebars		waveform
random			smptehdbars		weave
readeia608		sobel			xbr
readvitc		spectrumsynth		yadif
realtime		split			yuvtestsrc
remap			spp			zmq
removegrain		ssim			zoompan

Enabled bsfs:
aac_adtstoasc		hapqa_extract		mpeg4_unpack_bframes
chomp			hevc_metadata		noise
dca_core		hevc_mp4toannexb	null
dump_extradata		imx_dump_header		remove_extradata
eac3_core		mjpeg2jpeg		text2movsub
extract_extradata	mjpega_dump_header	trace_headers
filter_units		mov2textsub		vp9_raw_reorder
h264_metadata		mp3_header_decompress	vp9_superframe
h264_mp4toannexb	mpeg2_metadata		vp9_superframe_split
h264_redundant_pps

Enabled indevs:
fbdev			libcdio			v4l2
iec61883		libdc1394		xcbgrab
lavfi			oss

Enabled outdevs:
caca			oss			v4l2
fbdev
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
