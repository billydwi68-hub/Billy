import React, { useState } from 'react';
import { Button } from "/components/ui/button";
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from "/components/ui/card";
import { Input } from "/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Label } from "/components/ui/label";

const MotorRepaintWebsite = () => {
  const [name, billy] = useState('');
  const [email, billydwi68@gmail.com] = useState('');
  const [message, setMessage] = useState('');

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    // Handle form submission here
    console.log({ name, email, message });
    alert('Terima kasih! Pesan Anda telah dikirim.');
    setName('');
    setEmail('');
    setMessage('');
  };

  return (
    <div className="min-h-screen bg-background">
      {/* Header */}
      <header className="bg-primary text-primary-foreground py-6">
        <div className="container mx-auto px-4">
          <div className="flex justify-between items-center">
            <h1 className="text-2xl font-bold">MotorColor Repaint</h1>
            <nav className="hidden md:flex space-x-6">
              <a href="#services" className="hover:text-accent transition-colors">Layanan</a>
              <a href="#products" className="hover:text-accent transition-colors">Produk</a>
              <a href="#about" className="hover:text-accent transition-colors">Tentang</a>
              <a href="#contact" className="hover:text-accent transition-colors">Kontak</a>
            </nav>
            <Button variant="secondary" className="md:hidden">Menu</Button>
          </div>
        </div>
      </header>

      {/* Hero Section */}
      <section className="bg-gradient-to-r from-primary to-primary/80 text-primary-foreground py-20">
        <div className="container mx-auto px-4 text-center">
          <h2 className="text-4xl md:text-6xl font-bold mb-6">Jasa Repaint Motor Profesional</h2>
          <p className="text-xl md:text-2xl mb-8">Transformasi motor Anda dengan hasil cat yang sempurna dan tahan lama</p>
          <div className="flex flex-col sm:flex-row gap-4 justify-center">
            <Button size="lg" className="bg-accent text-accent-foreground hover:bg-accent/90">
              Konsultasi Gratis
            </Button>
            <Button variant="outline" size="lg" className="border-primary-foreground text-primary-foreground">
              Lihat Katalog
            </Button>
          </div>
        </div>
      </section>

      {/* Services Section */}
      <section id="services" className="py-20 bg-muted">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl md:text-4xl font-bold text-center mb-12">Layanan Kami</h2>
          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
            {/* Service 1 */}
            <Card className="bg-background">
              <CardHeader>
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Professional motorcycle repaint service with skilled painter working on sport bike&id=service1-motor-repaint" 
                  alt="Layanan repaint motor profesional dengan painter terampil sedang bekerja pada motor sport"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
                <CardTitle>Repaint Full Body</CardTitle>
                <CardDescription>Cat ulang keseluruhan body motor dengan hasil sempurna</CardDescription>
              </CardHeader>
              <CardContent>
                <p className="text-muted-foreground">Mulai dari Rp 1.500.000</p>
                <ul className="mt-4 space-y-2">
                  <li className="flex items-center">âœ“ Persiapan surface profesional</li>
                  <li className="flex items-center">âœ“ Cat berkualitas tinggi</li>
                  <li className="flex items-center">âœ“ Garansi 1 tahun</li>
                </ul>
              </CardContent>
              <CardFooter>
                <Button className="w-full">Pesan Sekarang</Button>
              </CardFooter>
            </Card>

            {/* Service 2 */}
            <Card className="bg-background">
              <CardHeader>
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Custom motorcycle design with intricate patterns and metallic colors&id=service2-custom-design" 
                  alt="Desain motor custom dengan pola intricate dan warna metallic"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
                <CardTitle>Custom Design</CardTitle>
                <CardDescription>Desain custom sesuai keinginan dengan berbagai pilihan efek</CardDescription>
              </CardHeader>
              <CardContent>
                <p className="text-muted-foreground">Mulai dari Rp 2.500.000</p>
                <ul className="mt-4 space-y-2">
                  <li className="flex items-center">âœ“ Desain eksklusif</li>
                  <li className="flex items-center">âœ“ Efek pearl dan metallic</li>
                  <li className="flex items-center">âœ“ Konsultasi gratis</li>
                </ul>
              </CardContent>
              <CardFooter>
                <Button className="w-full">Pesan Sekarang</Button>
              </CardFooter>
            </Card>

            {/* Service 3 */}
            <Card className="bg-background">
              <CardHeader>
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Motorcycle touch-up repair with painter fixing small scratches&id=service3-touch-up" 
                  alt="Perbaikan touch-up motor dengan painter memperbaiki goresan kecil"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
                <CardTitle>Touch-up & Perbaikan</CardTitle>
                <CardDescription>Perbaikan bagian tertentu dan touch-up untuk hasil seperti baru</CardDescription>
              </CardHeader>
              <CardContent>
                <p className="text-muted-foreground">Mulai dari Rp 500.000</p>
                <ul className="mt-4 space-y-2">
                  <li className="flex items-center">âœ“ Perbaikan goresan</li>
                  <li className="flex items-center">âœ“ Color matching presisi</li>
                  <li className="flex items-center">âœ“ Proses cepat</li>
                </ul>
              </CardContent>
              <CardFooter>
                <Button className="w-full">Pesan Sekarang</Button>
              </CardFooter>
            </Card>
          </div>
        </div>
      </section>

      {/* Products Section */}
      <section id="products" className="py-20 bg-background">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl md:text-4xl font-bold text-center mb-12">Produk Cat Motor</h2>
          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            {/* Product 1 */}
            <Card className="bg-muted">
              <CardHeader className="p-0">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/300x300?prompt=High quality motorcycle paint cans with metallic finish&id=product1-metallic-paint" 
                  alt="Kaleng cat motor berkualitas tinggi dengan finish metallic"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
              </CardHeader>
              <CardContent className="p-4">
                <CardTitle>Cat Metallic</CardTitle>
                <CardDescription>Efek kilau metalik yang mewah</CardDescription>
                <p className="text-primary font-bold mt-2">Rp 250.000 / kaleng</p>
              </CardContent>
              <CardFooter className="p-4 pt-0">
                <Button className="w-full">Beli Sekarang</Button>
              </CardFooter>
            </Card>

            {/* Product 2 */}
            <Card className="bg-muted">
              <CardHeader className="p-0">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/300x300?prompt=Pearl effect motorcycle paint with iridescent quality&id=product2-pearl-paint" 
                  alt="Cat motor efek pearl dengan kualitas iridescent"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
              </CardHeader>
              <CardContent className="p-4">
                <CardTitle>Cat Pearl</CardTitle>
                <CardDescription>Efek mutiara yang elegan</CardDescription>
                <p className="text-primary font-bold mt-2">Rp 300.000 / kaleng</p>
              </CardContent>
              <CardFooter className="p-4 pt-0">
                <Button className="w-full">Beli Sekarang</Button>
              </CardFooter>
            </Card>

            {/* Product 3 */}
            <Card className="bg-muted">
              <CardHeader className="p-0">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/300x300?prompt=Matte finish motorcycle paint in various colors&id=product3-matte-paint" 
                  alt="Cat motor finish matte dalam berbagai warna"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
              </CardHeader>
              <CardContent className="p-4">
                <CardTitle>Cat Matte</CardTitle>
                <CardDescription>Finish matte yang trendy</CardDescription>
                <p className="text-primary font-bold mt-2">Rp 200.000 / kaleng</p>
              </CardContent>
              <CardFooter className="p-4 pt-0">
                <Button className="w-full">Beli Sekarang</Button>
              </CardFooter>
            </Card>

            {/* Product 4 */}
            <Card className="bg-muted">
              <CardHeader className="p-0">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/300x300?prompt=Clear coat protection for motorcycle paint&id=product4-clear-coat" 
                  alt="Pelindung clear coat untuk cat motor"
                  className="w-full h-48 object-cover rounded-t-lg"
                />
              </CardHeader>
              <CardContent className="p-4">
                <CardTitle>Clear Coat</CardTitle>
                <CardDescription>Pelindung akhir yang tahan lama</CardDescription>
                <p className="text-primary font-bold mt-2">Rp 150.000 / kaleng</p>
              </CardContent>
              <CardFooter className="p-4 pt-0">
                <Button className="w-full">Beli Sekarang</Button>
              </CardFooter>
            </Card>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="py-20 bg-muted">
        <div className="container mx-auto px-4">
          <div className="grid md:grid-cols-2 gap-12 items-center">
            <div>
              <img 
                src="https://placeholder-image-service.onrender.com/image/500x400?prompt=Professional motorcycle painting workshop with various tools and equipment&id=about-workshop" 
                alt="Workshop pengecatan motor profesional dengan berbagai alat dan peralatan"
                className="w-full rounded-lg shadow-lg"
              />
            </div>
            <div>
              <h2 className="text-3xl md:text-4xl font-bold mb-6">Tentang MotorColor</h2>
              <p className="text-muted-foreground mb-4">
                Sejak 2015, MotorColor telah menjadi pilihan utama para pecinta motor untuk jasa repaint dan produk cat berkualitas. 
                Kami mengutamakan kualitas, ketelitian, dan kepuasan pelanggan.
              </p>
              <p className="text-muted-foreground mb-6">
                Dengan tim painter profesional dan berpengalaman, kami siap mewujudkan impian Anda untuk memiliki motor dengan tampilan yang sempurna.
              </p>
              <div className="grid grid-cols-2 gap-4">
                <div className="text-center">
                  <div className="text-2xl font-bold text-primary">500+</div>
                  <div className="text-muted-foreground">Motor Terlayani</div>
                </div>
                <div className="text-center">
                  <div className="text-2xl font-bold text-primary">8+</div>
                  <div className="text-muted-foreground">Tahun Pengalaman</div>
                </div>
                <div className="text-center">
                  <div className="text-2xl font-bold text-primary">98%</div>
                  <div className="text-muted-foreground">Kepuasan Pelanggan</div>
                </div>
                <div className="text-center">
                  <div className="text-2xl font-bold text-primary">1 Tahun</div>
                  <div className="text-muted-foreground">Garansi</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-20 bg-background">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl md:text-4xl font-bold text-center mb-12">Hubungi Kami</h2>
          <div className="grid md:grid-cols-2 gap-12">
            <div>
              <h3 className="text-2xl font-bold mb-6">Informasi Kontak</h3>
              <div className="space-y-4">
                <div>
                  <h4 className="font-semibold">Alamat</h4>
                  <p className="text-muted-foreground">Jl. Raya Motor No. 123, Jakarta Selatan</p>
                </div>
                <div>
                  <h4 className="font-semibold">Telepon</h4>
                  <p className="text-muted-foreground">+62 812-3456-7890</p>
                </div>
                <div>
                  <h4 className="font-semibold">Email</h4>
                  <p className="text-muted-foreground">info@motorcolor.com</p>
                </div>
                <div>
                  <h4 className="font-semibold">Jam Operasional</h4>
                  <p className="text-muted-foreground">Senin - Sabtu: 09:00 - 18:00</p>
                </div>
              </div>
              <div className="mt-8">
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Motorcycle workshop location map in Jakarta&id=contact-map" 
                  alt="Peta lokasi workshop motor di Jakarta"
                  className="w-full rounded-lg shadow-md"
                />
              </div>
            </div>
            <div>
              <Card>
                <CardHeader>
                  <CardTitle>Kirim Pesan</CardTitle>
                  <CardDescription>Kami akan membalas dalam 24 jam</CardDescription>
                </CardHeader>
                <CardContent>
                  <form onSubmit={handleSubmit} className="space-y-4">
                    <div className="space-y-2">
                      <Label htmlFor="name">Nama Lengkap</Label>
                      <Input
                        id="name"
                        value={name}
                        onChange={(e) => setName(e.target.value)}
                        required
                      />
                    </div>
                    <div className="space-y-2">
                      <Label htmlFor="email">Email</Label>
                      <Input
                        id="email"
                        type="email"
                        value={email}
                        onChange={(e) => setEmail(e.target.value)}
                        required
                      />
                    </div>
                    <div className="space-y-2">
                      <Label htmlFor="message">Pesan</Label>
                      <Textarea
                        id="message"
                        value={message}
                        onChange={(e) => setMessage(e.target.value)}
                        rows={5}
                        required
                      />
                    </div>
                    <Button type="submit" className="w-full">
                      Kirim Pesan
                    </Button>
                  </form>
                </CardContent>
              </Card>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-primary text-primary-foreground py-12">
        <div className="container mx-auto px-4">
          <div className="grid md:grid-cols-3 gap-8">
            <div>
              <h3 className="text-xl font-bold mb-4">MotorColor</h3>
              <p className="text
            -primary-foreground/80">
                Jasa repaint motor profesional dan penjualan produk cat motor berkualitas.
              </p>
            </div>
            <div>
              <h3 className="text-xl font-bold mb-4">Link Cepat</h3>
              <ul className="space-y-2">
                <li><a href="#services" className="text-primary-foreground/80 hover:text-accent">Layanan</a></li>
                <li><a href="#products" className="text-primary-foreground/80 hover:text-accent">Produk</a></li>
                <li><a href="#about" className="text-primary-foreground/80 hover:text-accent">Tentang</a></li>
                <li><a href="#contact" className="text-primary-foreground/80 hover:text-accent">Kontak</081228174622></li>
              </ul>
            </div>
            <div>
              <h3 className="text-xl font-bold mb-4">Follow Kami</h3>
              <div className="flex space-x-4">
                <a href="#" className="text-primary-foreground/80 hover:text-accent">Instagram</billydwi_93>
                <a href="#"className="text-primary-foreground/80 hover:text-accent">Facebook</bill creator>
                <a href="#" className="text-primary-foreground/80 hover:text-accent">YouTube</a>
              </div>
            </div>
          </div>
          <div className="border-t border-primary-foreground/20 mt-8 pt-8 text-center">
            <p className="text-primary-foreground/60">Â© 2024 MotorColor. All rights reserved.</p>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default MotorRepaintWebsite;
